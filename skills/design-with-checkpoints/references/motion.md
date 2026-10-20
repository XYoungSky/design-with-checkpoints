# Motion

The values below are starting points. Look at the result at normal speed, adjust, and give the reason when you depart from them.

## Give every animation a job

| Job | What it does | Example |
| --- | --- | --- |
| Feedback | Confirms that input was received | A button presses in; a toggle slides |
| Orientation | Shows where something came from or went | A drawer slides from its edge; a card expands into a detail view |
| Attention | Points to a change the user might miss | A new row highlights briefly |
| Narrative and character | Tells a short story or expresses the brand at a rare moment | A hero entrance; a product demo; a success moment |

If none applies, change the state instantly.

## Choose an intensity

Motion intensity is a design choice, like density or type contrast. Offer it in checkpoint 2 and show each level at normal speed.

| Level | Feel | Adds | Default for |
| --- | --- | --- | --- |
| Calm | Quiet and immediate | Feedback and orientation only | Dashboards, tools, forms, documentation |
| Lively | Polished and alive | One choreographed hero entrance, section headings revealed as they scroll in, springy layout changes, richer micro-interactions | Marketing pages, portfolios, product launches |
| Expressive | A showpiece | Pointer-reactive depth on illustrations, scroll-linked storytelling, page transitions, blur and 3D on decorative layers | Campaigns, brand sites, demos |

Richness goes where motion is rare and attention is welcome. At every level, high-frequency interactions keep the frequency budget below.

## Let frequency set the budget

| Frequency | Examples | Budget |
| --- | --- | --- |
| High: many times per session | Hover, tabs, toggles, typing, filters | 150ms or less, or none |
| Medium | Menus, popovers, accordions, dialogs, demo steps | 150–350ms; up to 550ms with a spring |
| Low: once per visit or less | First load, section entrances, page transitions, onboarding | Up to 1.2s in total; may be expressive |

## Make it rich, keep it reasonable

- One focal moment per screen. Everything else supports it or stays still.
- Primary content is readable within 400ms of first paint, even while decoration is still arriving.
- An entrance plays once, or is tied to the scroll position. It never replays on a timer.
- Overshoot stays within about 5% for interface elements; decoration may move more.
- Animate headings by line, never body text by letter.
- Decorative layers may tilt, float, or parallax. Text and controls stay put.
- Input works at every moment of every animation.

## Techniques

- **Choreographed entrance:** stagger 60–100ms with overlapping durations, in reading order or from back to front.
- **Mask reveal:** `clip-path: inset(0 0 100% 0)` to `inset(0)` on heading lines. Layout stays stable while the text rises into view.
- **Spring:** use the project's library, or this CSS spring with about 4% overshoot: `linear(0, 0.16 7.5%, 0.45 15%, 0.72 22.5%, 0.89 30%, 0.99 37.5%, 1.03 45%, 1.038 50%, 1.03 60%, 1.015 70%, 1.005 80%, 1)`. For a small pop: `cubic-bezier(0.34, 1.56, 0.64, 1)`.
- **Shared element:** move elements to their new layout instead of jumping (FLIP, or the View Transitions API where supported).
- **Scroll-driven:** CSS `animation-timeline: view()` for section reveals and progress indicators. Native scrolling stays intact; browsers without support show the final state.
- **Depth:** layered parallax or a pointer tilt of 8° or less on illustrations, only on devices with a fine pointer.
- **Drawn lines:** reveal rules and connectors with `scaleX` or SVG `stroke-dashoffset`.

## Starting values

| Interaction | Duration | Easing |
| --- | --- | --- |
| Hover and press feedback | 100–150ms; scale to 0.97 on press | ease-out |
| Tooltip, dropdown | 120–220ms in, 100–150ms out | ease-out in, ease-in out |
| Accordion | 180–250ms | ease-in-out on height |
| Drawer, dialog | 220–320ms in, about two-thirds of that out | ease-out in, ease-in out |
| Layout change, shared element | 300–550ms | spring, or ease-in-out |
| Section heading reveal | 400–600ms, or tied to scroll | ease-out |
| Hero entrance | 600–1200ms in total, 60–100ms stagger | ease-out and spring |

Curves: ease-out `cubic-bezier(0.22, 1, 0.36, 1)` for entering and responding; ease-in `cubic-bezier(0.55, 0, 1, 0.45)` for leaving; ease-in-out `cubic-bezier(0.65, 0, 0.35, 1)` for moving. Use linear only for opacity loops, progress bars, and spinners. Exits are faster than entrances.

## Off by default

Use these only when the user asks explicitly, and record the purpose in the inventory:

- scroll hijacking: intercepting wheel or touch input to control scrolling;
- a reveal on every element of the page, rather than on headings and key visuals;
- looping motion next to text people are reading;
- parallax on text, or letter-by-letter reveals of body text;
- content that stays hidden unless a script runs.

## Implementation

- Animate `transform`, `opacity`, `clip-path`, and `filter` on small elements. Check for dropped frames with a 4× CPU slowdown in DevTools.
- Prefer CSS transitions for state changes; they reverse from the current position. For sequences, use the Web Animations API or the project's library, and retarget from the current state on reversal.
- Write entrance keyframes with only a `from` state, so each element lands on its own resting style at every breakpoint.
- Cancel animations and listeners on unmount, route change, and resize. Never depend on `animationend` to reach a valid state.
- Hidden or exiting content must not receive focus or clicks; use `inert`.

## Reduced motion

Under `prefers-reduced-motion: reduce`, show the final state, or use a fade of 150ms or less. Keep every piece of content, state, and control, across CSS, JavaScript, scroll-driven effects, and video. Content that moves for more than 5 seconds also needs a pause control.

## Motion inventory

List every animation in the delivered work, and the chosen intensity at the top. The user sees it three times: as a draft for each direction at checkpoint 2, in full at the sample review, and in its final form in the delivery report. Write it in the user's language with plain column names; for a Chinese-speaking user: 元素 · 触发 · 用途 · 频率 · 时长与曲线 · 中途打断 · 减弱动效时.

| Element | Trigger | Job | Frequency | Duration and easing | Interruption | Reduced motion |
| --- | --- | --- | --- | --- | --- | --- |
| Hero heading | First load | Narrative | Low | 700ms mask reveal, 80ms stagger per line | Plays once | Visible immediately |
| Filter drawer | Tap "Filter" | Orientation | Medium | 260ms ease-out in, 180ms ease-in out | Reverses from current position | Instant |
| Save button | Press | Feedback | High | 120ms, scale 0.97 | Not needed | Color change only |

Rules:

- No job means the animation is removed.
- High frequency with a duration over 150ms needs a written reason, or a shorter duration.
- Test every row at normal speed, with rapid repeated input, and with reduced motion on.

## Asking about motion

Ask about intensity with a sample of each level, using the same content, and recommend one for the product type. Do not ask the user to choose durations or curves; choose them from the tables and tune them by eye.
