# Sources and Evidence Limits

Use these sources to understand the workflow's origins and limits. This package expresses a synthesis in its own structure and wording; it does not imply endorsement by the source authors or rank the “best skill.” The research snapshot is dated 2026-10-06. Recheck original material and versions when current APIs, standards, or code reuse matter.

## Evidence status and claim boundaries

- **Normative:** WCAG success criteria and conformance rules specify requirements for a named target. Apply the actual version, level, scope, and exceptions. The linked Understanding documents and APG explain implementation; they are not themselves normative WCAG requirements. Do not infer a project's legal obligations from a standard link.
- **Technical guidance:** browser/vendor documentation explains measurement and implementation mechanics. Verify the project's actual browser, dependency version, and trace; a recommended technique is not evidence that an implementation passed.
- **Method or heuristic:** professional design methods and practitioner skills guide judgment. Their authority, popularity, examples, or claims do not demonstrate universal causal benefits.
- **Project evidence:** task observations, controlled measurements, and user choices answer different questions. Preserve methods, raw results, limitations, and proposed versus validated values. User preference is valid evidence of preference, not proof of conversion or usability gains.

The workflow's requirement-to-test chain, parameter experiments, and regression cases are this package's operational synthesis. They make claims reviewable and falsifiable; they do not make aesthetic taste scientifically proven.

## Primary method sources

### Derive design from tasks and content

- [Anthropic frontend-design](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md): use a concrete brief to form a visual direction and check generic tendencies. Do not treat it as a complete requirements, acceptance, or publishing process.
- [Leonxlnx taste-skill](https://github.com/Leonxlnx/taste-skill): audit before redesigning and distinguish layout, density, and motion intensity. Do not inherit universal aesthetic bans, default parameters, or framework preferences.
- [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill): research specific design or technical questions. Treat categories and search results as candidate support, not automatic brand decisions. This package does not depend on its search program.

### Separate research, comparison, and implementation

- [Matt Pocock grilling](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md) and the [grill-me entry point](https://github.com/mattpocock/skills/blob/main/skills/productivity/grill-me/SKILL.md): resolve prerequisites, include recommendations, and adapt the next question to the answer. The 1–3-question round is this package's interaction choice, not a claimed fixed rule from those sources.
- [Design Council Double Diamond](https://www.designcouncil.org.uk/resources/the-double-diamond/): use discovery, definition, development, and delivery, revisiting the problem when needed. Do not turn exploration into fixed linear approvals.
- [GOV.UK Making prototypes](https://www.gov.uk/service-manual/design/making-prototypes): test assumptions at an appropriate fidelity and distinguish prototypes from production quality. Its toolkit is not required.
- [Shape Up: Find the Elements](https://basecamp.com/shapeup/1.3-chapter-04): discuss structure and key tasks before premature pixel detail. Do not import its team cadence or cycle system.

### Ground audits and compare directions

- [ibelick create-design-md](https://github.com/ibelick/ui-skills/blob/main/skills/create-design-md/SKILL.md) and [baseline-ui](https://github.com/ibelick/ui-skills/blob/main/skills/baseline-ui/SKILL.md): distinguish source code, computed styles, and observed evidence; preserve product identity and basic interaction quality. Do not turn a local baseline into every project's aesthetic direction.
- [Emil prototype](https://github.com/emilkowalski/skills/blob/main/skills/prototype/SKILL.md): compare operable candidates at real usage size before integrating a choice. This package chooses 2–3 directions and a first-screen-plus-key-segment scope for website work.
- [Impeccable](https://github.com/pbakaus/impeccable): distinguish product facts, design decisions, and page tasks; separate design critique, technical review, and finishing. This package does not import its installer, engine, hooks, commands, or concept-assignment mechanisms.

### Design motion and verify actual behavior

- [Emil skills](https://github.com/emilkowalski/skills), [review-animations](https://github.com/emilkowalski/skills/blob/main/skills/review-animations/SKILL.md), and [Train Your Judgement](https://emilkowal.ski/ui/train-your-judgement): judge purpose, frequency, repeated use, interruption, and paired comparisons. Determine actual timing, easing, and amplitude through project experiments.
- [Anthropic: Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps): separate generation from actual browser review and preserve intermediate versions. This first-party experiment does not establish equal results across other models, projects, or budgets, and does not justify unlimited review loops.

## Technical verification entry points

### Accessibility standards and implementation guidance

- [WCAG 2.2](https://www.w3.org/TR/WCAG22/): normative criteria and conformance rules. The focused checks in [Motion and QA](motion-and-qa.md) do not replace a full audit.
- Understanding documents: [text contrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [non-text contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html), [reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html), [text resizing](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html), and [text spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html). Apply scope/exceptions; spacing override tests do not prescribe default typography.
- [Focus Not Obscured (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html) and [Target Size (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html): AA criteria; distinguish stricter AAA criteria and project choices.
- [Animation from Interactions](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html), [Pause, Stop, Hide](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html), and [Three Flashes or Below Threshold](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold.html): separate interaction animation (AAA), applicable moving/updating content (A), and flash safety (A).
- [WAI-ARIA APG patterns](https://www.w3.org/WAI/ARIA/apg/patterns/), [keyboard interface](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/), and [modal dialog](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/): choose pattern-specific semantics and focus behavior. APG patterns are implementation guidance, not automatic conformance.

### Frontend structure, motion, and measurement

- [Design Tokens Format Module 2025.10](https://www.designtokens.org/tr/2025.10/format/): types, groups, and aliases for token interchange. A Design Tokens Community Group specification, not a W3C Recommendation; optional when useful to the existing workflow.
- [CSS Transitions Level 1](https://www.w3.org/TR/css-transitions-1/): CSS-specific interruption and reversing behavior. Do not assume other animation APIs share every rule.
- [web.dev Animation performance guide](https://web.dev/articles/animations-guide) and [Chrome Performance panel](https://developer.chrome.com/docs/devtools/performance/): use rendering/runtime evidence rather than property-name or frame-rate promises.
- [web.dev Reduced motion](https://web.dev/articles/prefers-reduced-motion): implement and test the system preference across relevant effects, preserving meaning and operation.
- [web.dev Web Vitals](https://web.dev/articles/vitals), [threshold rationale](https://web.dev/articles/defining-core-web-vitals-thresholds), and [INP optimization](https://web.dev/articles/optimize-inp): field distributions, lab diagnostics, and interaction timing have distinct roles. Do not substitute a navigation score for field evidence.
- [Playwright Emulation](https://playwright.dev/docs/emulation): device-parameter emulation does not establish physical-device behavior.

### Usability and evaluation

- [GOV.UK moderated usability testing](https://www.gov.uk/service-manual/user-research/using-moderated-usability-testing): neutral, realistic tasks and observed behavior. Adapt to the research question and authorized participants; do not generalize a small sample into a population effect.
- [WAI: involving users in evaluation](https://www.w3.org/WAI/test-evaluate/involving-users/): combine individual user findings with standards-based assessment; neither replaces the other.
- The official skill-creator guidance supplied by the host: progressive disclosure, proportionate workflows, structural validation, and independent forward-testing. Use its installed validator if available; do not claim its frontmatter checks establish behavioral effectiveness.

## Use community reports as leads, not rankings

Use the reports below to identify risks and design validation scenarios. They do not isolate the effects of model, brief, assets, stack, or operator and do not establish an effectiveness ranking.

- [Taste issue #86](https://github.com/Leonxlnx/taste-skill/issues/86): consider conflicts between generic aesthetic restrictions, semantic states, and technology stacks; define project-specific exceptions.
- [Reddit: generic results after months of combining frontend skills](https://www.reddit.com/r/ClaudeAI/comments/1t24gan/few_months_of_frontenddesign_uiuxpromaxskill/): preserve project decisions and prevent discarded patterns from returning. Do not interpret this report as a universal rejection of any skill.
- [Hacker News: Impeccable Style](https://news.ycombinator.com/item?id=46587284): peer criticism of early examples highlights how visual changes may harm readability or task emphasis. Do not automatically apply those criticisms to later versions.

The research did not establish an independent, multi-sample comparison of all six approaches under the same model, brief, and budget. Stars, installations, curated showcases, model self-scores, and detector pass rates cannot fill that evidence gap.

## Respect reuse boundaries

This package includes no third-party source code, assets, executables, or installation dependencies. It imports no upstream commands and runs no upstream hooks. It restates methods in its own structure and wording while linking their origins.

Before directly copying, translating, or adapting source passages, code, or assets, verify the exact file, version, license, and attribution/change-notice requirements. These links do not establish that permission has already been obtained. Verify different repositories and external registry entries separately. Public access does not grant reuse rights to reference-site branding, photography, or distinctive work.

Evaluate this package on varied real tasks. Preserve the initial, post-selection, and final versions with actual browser defects. Compare task fit, hierarchy, interaction, mobile behavior, and rework cost. Report only evidenced benefits and limitations; do not claim a universally optimal workflow.
