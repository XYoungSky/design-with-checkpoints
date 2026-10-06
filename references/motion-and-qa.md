# Motion and QA

Contents: [state/focus](#specify-interaction-before-animation) · [choreography](#decide-why-an-element-should-move) · [reduced motion](#preserve-functionality-with-reduced-motion) · [accessibility](#turn-accessibility-criteria-into-explicit-checks) · [test matrix](#build-a-project-specific-test-matrix) · [visual review](#inspect-visuals-in-addition-to-build-results) · [performance](#match-performance-claims-to-evidence) · [delivery](#accept-deliver-and-verify-publication).

## Specify interaction before animation

For each consequential component, enumerate logical states and events: idle, focused, expanded/selected, loading, empty, error, success, and disabled only where relevant. Map event → state change → visible feedback → accessible state/name → focus destination. Keep transient animation phases distinct from the logical state. Specify cancellation, stale async responses, retries, duplicate activation, and navigation-away behavior where the component has those risks.

Prefer native HTML behavior and the existing accessible component system. Use a matching [WAI-ARIA APG pattern](https://www.w3.org/WAI/ARIA/apg/patterns/) for custom widgets; APG is implementation guidance, not a WCAG conformance certificate. Do not apply menu or dialog keyboard behavior to every navigation disclosure.

For a modal, define initial focus, keyboard containment, dismissal, background inertness, and focus return, including a logical fallback if the trigger disappears; see the [APG modal pattern](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/). For non-modal disclosure, preserve ordinary page navigation unless its pattern requires otherwise. Distinguish focus from selection and follow the component-specific arrow-key/Tab model, as explained in [keyboard-interface guidance](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/). Announce meaningful async status without moving focus unnecessarily or flooding a live region.

## Decide why an element should move

Give each major animation a clear purpose: acknowledge input, explain state or spatial relationships, direct attention, or support necessary narrative. Otherwise start with an immediate state change. Do not automatically add scroll hijacking, floating loops, word-by-word reveals, or 3D to enrich a demonstration.

Distinguish frequent operational feedback from infrequent presentation moments. Prioritize responsiveness and interruption for frequent actions; reserve more pronounced choreography for justified moments. Choose intensity using real content and repeated use rather than applying one duration or curve everywhere.

Define a minimal contract for important motion:

- Target element, user purpose, trigger, and termination conditions.
- Start/end states, changing properties, initial timing/easing or spring parameters; label experimental values.
- Repeated triggers, reversal during playback, and immediate exit after entry.
- Focus, scroll locking, clickability, keyboard, and touch behavior.
- Cleanup on route changes, page blur, and component unmount.
- Reduced-motion alternative, performance measurement, and acceptance criteria.

Define choreography as relationships, not a list of effects: which elements move together, which depend on a prior state, the focal element, spatial origin, overlap/stagger, and total time until the task is usable. Avoid accumulating per-item delays that make long lists progressively slower. Specify duration and delay in ms, displacement in an appropriate unit, transform origin, property-specific easing or the chosen library's spring parameters. Explain any difference between entry and exit. Values remain experimental until tested.

Choose the repeated-input policy explicitly: retarget/reverse from the current visual state for reversible UI, or a justified guard/queue for a transactional operation. Never replay from a stale start frame by accident. Test open → close → open while the prior transition is still running, resize/content change mid-transition, and route/unmount cleanup. CSS transitions define interrupted/reversed behavior; consult the [CSS Transitions specification](https://www.w3.org/TR/css-transitions-1/) when relying on those mechanics rather than assuming every animation API behaves the same.

Do not queue decorative motion ahead of essential input, focus, status, or navigation. Keep hidden/exiting content from receiving unintended focus or clicks; synchronize semantics, inertness, and cleanup deliberately. A completion callback may clean up visuals, but it must not be the only path to usable content or a valid state. Test both cancellation and a skipped animation.

Inspect normal speed in a real browser, then try repeated input. If slowed playback helps diagnosis, record a separate conclusion about normal speed. A screenshot proves only one frame; a recording alone cannot establish interactive-state correctness or measured performance.

## Preserve functionality with reduced motion

Cover both CSS and JavaScript animations. Under the system's reduced-motion preference, replace unnecessary motion with the final state or clear low-motion feedback. Preserve all content, navigation, and state information. Do not make core functionality depend on an animation-end event.

If the user asks to remove a page-level reduced-motion toggle, remove only that control and its necessary associated logic. Preserve system-preference support and testing. Do not indiscriminately set every duration to zero and cause races, invisible content, leftover overlays, or deadlocks.

Check applicable pause, stop, and hide requirements separately for autoplaying content. Reduced-motion support does not replace every control requirement. Supporting one media query does not establish conformance with a complete accessibility level.

Treat the system preference as an input to the entire choreography, including CSS, JavaScript, scroll effects, and looping media. If a preference changes during playback, settle safely to a usable state. Follow [reduced-motion implementation guidance](https://web.dev/articles/prefers-reduced-motion); do not assume “lower duration” alone addresses large spatial motion.

## Turn accessibility criteria into explicit checks

Use the project's selected target; propose WCAG 2.2 AA when none is established, without claiming a legal obligation or completed conformance audit. The normative [WCAG 2.2 standard](https://www.w3.org/TR/WCAG22/) governs conformance; Understanding pages explain it. The checks below are relevant examples, not a complete audit:

- Text contrast: test actual foreground/background pairs in required states, including imagery and transparency. [1.4.3, AA](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) generally requires 4.5:1, or 3:1 for its defined large text; document applicable exceptions. Do not infer pass from a palette swatch alone.
- UI/state contrast: [1.4.11, AA](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) requires 3:1 for visual information necessary to identify enabled controls/states and relevant graphics, with stated exceptions. This is not a blanket ratio requirement for every decorative boundary.
- Reflow: [1.4.10, AA](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) tests without loss or requiring scrolling in two dimensions at 320 CSS px width for vertically scrolling content, or 256 CSS px height for horizontally scrolling content; evaluate its scoped two-dimensional-content exceptions. A 1280 CSS px viewport at 400% zoom can exercise the 320-width case; test actual results.
- Enlargement and spacing: test [text enlargement to 200%](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html) and [1.4.12 spacing overrides](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html) without loss. Apply these overrides simultaneously, without changing other style properties: line height 1.5×, spacing after paragraphs 2×, letter spacing 0.12×, and word spacing 0.16×, each relative to font size. These are test conditions, not mandatory default typography. Apply only spacing properties used by the language/script.
- Focus: test keyboard operation, visible focus, meaningful order, and [2.4.11, AA](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html): author content must not completely hide the focused component, subject to its notes. Keeping it fully unobscured is a useful stronger goal, distinct from the AA minimum; 2.4.12 and 2.4.13 are AAA.
- Pointer targets: [2.5.8, AA](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html) uses 24 × 24 CSS px or its spacing/other exceptions. A chosen 44 × 44 target is a project design choice or part of the distinct 2.5.5 AAA criterion, not the AA minimum.
- Motion/media: [2.3.3 interaction animation, AAA](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html), [2.2.2 pause/stop/hide, A](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html), and [2.3.1 flash safety, A](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold.html) address different conditions. Apply their actual scope and exceptions; support reduced motion as a project safeguard even when AAA is not the selected target.

Also test semantics, accessible names, labels/errors, status messages, and relevant assistive-technology behavior. Automated scans cover only part of the criteria. User acceptance of a limitation does not turn a known failure into conformance.

## Build a project-specific test matrix

Record the version, URL, browser/engine, viewport, zoom, input method, system preferences, and data state. Use the following as starting points, not a mandatory fixed device list:

- Responsive layout: prioritize audience-relevant sizes, then narrow/wide viewports, both sides of breakpoints, and continuous resizing. Possible samples include 320, 390, 768, 1280, and 1440 CSS px. Use 320 for reflow checks, not as a proxy for every phone.
- Zoom and reflow: inspect necessary content and functionality with text enlargement and page zoom. Record actual conditions. Analyze essential two-dimensional layouts separately rather than forcing everything into one column.
- Input: test mouse, keyboard, and touch; Tab/Shift+Tab, Enter/Space, and Escape; visible focus, logical order, and focus restoration. Provide keyboard and touch access to hover information.
- Content: use real Chinese/English where relevant, long headings, missing values, long lists, failed images, unloaded fonts, and loading/success/error states. Check wrapping, baselines, reading width, cropping, and hierarchy.
- Copy/localization: inspect the full page and all interaction states, including headings, navigation, CTAs, forms, empty/loading/error messages, tooltips, permission notices, and accessible names. Newly authored text defaults to the conversation language; any alternative or bilingual treatment must be chosen. Preserve protected source copy. Remove affected faux-gentle/poetic filler and redundant ambient meta explanations; retain concise actionable recovery, access, security, consent, and legal information where needed. Check action labels match behavior and avoid unexplained language switching.
- Paths: test primary calls to action, navigation, internal/external links, deep links, refresh, and browser back/forward. Test forms in a safe environment or with approved data; do not send real messages, orders, or external submissions without authorization.
- Motion: rapidly retrigger, reverse during playback, alternate opening/closing, reverse scrolling, return immediately, change routes, and blur/refocus the page. Check residual styles, overlays, scroll locks, and inconsistent state.
- System preferences: test both `no-preference` and `reduce`. If the implementation listens for preference changes, also test changes during use.
- Browsers: run actual target browsers and list unavailable coverage. Distinguish Chromium mobile emulation, WebKit testing, and physical iPhone Safari testing accurately.
- Performance and reliability: inspect the console, failed requests, images/fonts, layout shifts, long tasks, and animation traces. Repeat measurements when needed and identify the environment.

## Inspect visuals in addition to build results

Inspect full pages and key states. Check first-glance hierarchy, text rhythm, whitespace and density, component relationships, image crops, cross-page consistency, and whether mobile still expresses the chosen direction. Compare screenshots with the brief, prototypes, and approved decisions rather than unrelated “premium” sites.

Separate two kinds of findings and provide evidence for each:

- Functional/quality defects: reproducible task blockers, incorrect states or content, and responsive or accessibility failures.
- Design judgments: hierarchy, rhythm, distinctiveness, or density that conflicts with the goal or chosen direction. Explain reasons and alternatives without presenting taste as an objective standard.

For substantial or uncertain changes, use an independent reviewer when available and permitted, with the same brief and version. Otherwise complete the available checks and identify them as self-review. Prioritize high-impact findings. Retest fixes under the original conditions. A higher self-score, clean scan, or successful build does not establish acceptance.

## Match performance claims to evidence

Use [web.dev's rendering guidance](https://web.dev/articles/animations-guide) to form a hypothesis about cost. Where appropriate, prefer changes that avoid repeated layout/paint, but `transform`/`opacity` do not guarantee compositor execution, low memory use, or smoothness. Record traces of the actual affected interaction; diagnose layout, paint, long tasks, dropped frames, large layers, and the device's refresh-rate budget. Avoid blanket `will-change` or a heavy dependency for a minor effect.

Set a project budget before tuning, grounded in the baseline, audience devices, critical task, and applicable delivery constraints. Record build/version, browser, hardware or emulation, viewport/refresh rate, CPU/network profile, cache state, data, task script, tool, run count, and raw results. Repeat controlled runs to expose variation; report the observed range and appropriate summary instead of selecting the best run. Define the measurement budget and stopping rule in advance; an inconclusive sample remains inconclusive.

Current [Core Web Vitals guidance](https://web.dev/articles/vitals) uses “good” thresholds of LCP ≤ 2.5 s, INP ≤ 200 ms, and CLS ≤ 0.1, assessed at the 75th percentile of field visits, separately for mobile and desktop. These are experience thresholds, not proof of usability, accessibility, or causation. They do not mean 75% of pages passed. Verify the current definitions before making a release claim.

Separate field data (source, time window, population, page/origin scope) from repeatable lab diagnostics. A Lighthouse navigation score or Total Blocking Time is not a measured field INP. Measure real interactions in a runtime trace for local diagnosis; see [INP optimization](https://web.dev/articles/optimize-inp) and [Chrome's Performance panel](https://developer.chrome.com/docs/devtools/performance/). A short local session cannot certify production percentiles. If field data, target hardware, or tools are unavailable, state the exact gap and leave those acceptance checks pending; do not add telemetry or production traffic without authorization.

## Accept, deliver, and verify publication

Record each defect's reproduction conditions, expected/actual behavior, user impact, evidence, fix, and retest. Do not recommend release while task-blocking or serious content, mobile, keyboard, or state issues remain. Let the informed user choose whether to fix, accept, or narrow scope around remaining issues.

Present an identified candidate and a consolidated change batch. Do not deploy every small adjustment directly to production. Follow the established preview/publishing mode and host policy. Check design choices, candidate acceptance, and permission for public actions separately; do not ask again for valid existing authorization.

Before publishing, complete necessary path, resource, responsive, and motion QA in a real preview. After publishing, use the current host's permitted checks to verify deployment and, where available, the production experience. State exactly which checks ran and what they establish.

Continue handling recoverable failures within authorized scope. Pause at the exact blocker if new permission is needed. Report deployment status, tested coverage, and unverified areas separately. Successful deployment does not establish a tested production experience.
