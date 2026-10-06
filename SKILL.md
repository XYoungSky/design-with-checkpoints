---
name: design-with-checkpoints
description: "Design, redesign, and review websites and frontend interfaces with adaptive user checkpoints and evidence-based verification. Use for frontend plans, information architecture, layout, typography, interaction, motion, or visual polish. Scale work to the requested outcome; exclude backend-only work."
---

# Design with Checkpoints

Turn user goals into usable, distinctive, verifiable frontend designs. Own professional recommendations and implementation within scope; involve the user in unresolved consequential choices and honor explicit delegation.

## Route the task

Read the request, project conventions, existing design decisions, and relevant code. Verify the target and discoverable facts yourself. Deliver the requested plan, review, or implementation: plans and reviews stop at recommendations and evidence limits unless implementation is requested.

Default to inspecting the relevant interface, completing a verifiable batch, checking its effects, and using feedback to determine the next step. The stages below are optional tools, not a checklist. Enter research or prototyping when it resolves a material uncertainty or the user requests it. Scale depth by uncertainty, impact, and rework cost, not just page count.

For local fixes: reproduce → identify the affected layout/state/token → make the smallest authorized change → retest the affected path and nearby regressions → report. For new designs, establish goals, real content, and a coherent direction before expanding. Resume settled work without restarting discovery.

Read only relevant reference sections at their point of use. Routine work can follow this entrypoint; reference examples and templates do not add deliverables to the user's request.

## Keep the user involved

- Ask only about unresolved, non-delegated choices that materially affect goals, content priority, direction, core interaction, scope, or rework. Usually ask 1–3 questions, with concrete evidence, a recommendation, viable alternatives, and their tradeoffs. Resolve dependent choices in order.
- Existing decisions and explicit delegation satisfy the relevant checkpoint. Keep consequential choices visible and preserve any review point the user requested. Silence is not approval; liking a reference is not approval of an entire redesign.
- Wait before work that depends on an unanswered consequential choice. Continue independent authorized work. Handle spacing, type sizes, timing, and other details within the chosen direction; reopen only decisions affected by new evidence or scope.
- For difficult tradeoffs, use [answerable questions](references/interview-and-decisions.md#make-questions-answerable) and [decision boundaries](references/interview-and-decisions.md#preserve-decisions-rather-than-complete-chats). Do not ask the user to choose technical parameters without explaining their effect.

## Preserve design quality

Use user tasks, real content, and established brand facts to guide information hierarchy, typography, layout, density, color, assets, and interaction. Form a coherent visual direction appropriate to the project; do not apply one palette, grid, font pairing, or motion intensity everywhere. Label temporary material; never invent clients, statistics, testimonials, or commitments.

Explain design choices in the user's language with concrete tradeoffs. New UI content follows explicit instructions → established project language and confirmed audience → conversation language as fallback. Preserve locales and protected copy; clarify material conflicts before translating. Avoid generic promotional slogans, forced intimacy, poetic reassurance, padded politeness, and implementation commentary. Use specific actions and facts, retaining necessary context. When authoring UI text, apply [natural interface copy](references/interview-and-decisions.md#write-natural-interface-copy).

Distinguish observed behavior, source inference, design judgment, and unverified claims. Screenshots do not prove interaction, builds do not prove usability, and emulation does not prove physical-device behavior. Use [evidence guidance](references/reference-evidence.md#classify-evidence-before-using-it) for consequential claims and [sources](references/sources.md) when checking standards, attribution, or third-party reuse.

## Audit and define

Before changing an existing interface, inspect the affected pages and states in a real browser when available. Broaden to representative templates and paths for shared or sitewide changes. Capture enough version, viewport, and interaction evidence to reproduce findings. Use source code to understand ownership and constraints. Without browser access, continue permitted checks and explicitly leave rendered behavior unverified.

Identify what to preserve, the highest-impact problems, and the intended outcome. Establish relevant acceptance criteria before implementation; do not lower them afterward to conceal failures. For broad audits, consult [audit coverage](references/reference-evidence.md#audit-the-project-before-collecting-inspiration). Reuse existing briefs; clarify only unsettled goals or constraints.

## Research and propose directions

Research when the direction or design mechanism is uncertain, existing evidence is insufficient, or the user requests exploration. Start with supplied references and related user tasks. Explain what transfers and why, rather than collecting inspiration links; use [focused research](references/reference-evidence.md#research-a-specific-problem).

For substantial direction exploration, compare 2–3 meaningful alternatives or the number requested. Keep real content and comparison conditions consistent; vary information order, layout, density, visual character, or interaction rather than only palettes. Show enough desktop and mobile context to judge the choice. Explain benefits, sacrifices, and unknowns, and recommend one. Use [direction comparisons](references/reference-evidence.md#turn-references-into-design-directions) when needed; do not manufacture alternatives for a settled direction.

## Prototype unresolved choices

Use a prototype when a consequential choice is difficult to judge directly, rework would be costly, or a sample is requested. Choose the smallest sufficient representation: content structure for ordering, visual samples for typography/layout, and operable controls for interaction. Build only within authorized scope; a plan can describe a proposed test without implementing it.

For experiments, define the question and failure condition, keep comparisons fair, and distinguish preference from observed task success. Follow [prototype guidance](references/reference-evidence.md#keep-prototypes-small-and-comparisons-real). An exploratory sample need only resolve its question; state unfinished behavior and do not present it as release-ready. At a requested sample review, show the checked version and wait before expanding.

## Implement within scope

Work in batches that produce an inspectable user path or coherent improvement. For larger builds, verify one complete slice before repeating its patterns across pages. Use real content and necessary responsive and exceptional states. Respect the existing stack, components, and design conventions; avoid automatic framework, library, or token-system additions.

Preserve consequential decisions and their rationale in existing project records. A small change can be explained in the handoff. Write a separate [frontend specification](references/project-templates.md#frontend-specification) only when requested or needed for complex behavior, cross-page coordination, or handoff. Document new agreements and relevant values rather than duplicating code. Formal IDs and separate records are optional; keep requirements, choices, and validation traceable at an appropriate scale.

## Verify, incorporate feedback, and deliver

Check the affected visual hierarchy, text, responsive layout, interactions, and accessibility. Expand coverage for shared components, global styles, and core paths. Use the relevant [QA checks](references/motion-and-qa.md#build-a-project-specific-test-matrix), not every check for every task. For important motion, verify [state/focus behavior](references/motion-and-qa.md#specify-interaction-before-animation), repeated input, interruption, cleanup, and [reduced motion](references/motion-and-qa.md#preserve-functionality-with-reduced-motion). Use performance measurements when relevant to the change, an observed issue, or an agreed target.

Retest fixes under their reproduction conditions. For substantial or uncertain work, use an independent reviewer when available and permitted; otherwise identify self-review. Actual user research follows [task-testing guidance](references/reference-evidence.md#check-task-success-not-only-preference); an agent walkthrough is not human usability evidence. Do not claim quality from a build or automated score alone.

Handle feedback through the [shortest affected loop](references/interview-and-decisions.md#take-the-shortest-feedback-loop): repair defects, group local adjustments, and revisit only affected direction or scope choices. Keep useful earlier versions. When acceptance is an agreed checkpoint, present an identified candidate and wait; otherwise deliver within existing authorization without adding confirmation steps.

Report what changed, consequential decisions, tested scope, and failed or unverified checks. Link existing records where useful; use [handoff fields](references/project-templates.md#acceptance-and-handoff) only as needed. Do not recommend release with unresolved serious functional, content, responsive, or accessibility problems.

When preview sharing or publishing is in scope, verify target, visibility, and authorization under host policies. Design approval, candidate acceptance, and public-action permission are distinct; do not reconfirm unchanged valid authorization. For release, follow [publication checks](references/motion-and-qa.md#accept-deliver-and-verify-publication), including recovery and permitted production verification. Deployment success alone does not establish a tested experience.

Stop when the requested deliverable and agreed checks are complete, or at a necessary decision blocker. Do not expand scope or continue polishing indefinitely.
