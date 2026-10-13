---
name: design-with-checkpoints
description: "Design, redesign, and review websites and frontend interfaces with adaptive user checkpoints and evidence-based verification. Use for frontend plans, information architecture, layout, typography, interaction, motion, or visual polish. Scale work to the requested outcome; exclude backend-only work."
---

# Design with Checkpoints

Turn user goals into usable, distinctive, verifiable frontend designs. Clarify needs through the required question checkpoints, own professional recommendations and implementation within scope, and honor explicit delegation.

## Route the task

Read the request, project conventions, existing design decisions, and relevant code. Verify the target and discoverable facts yourself. Deliver the requested plan, review, or implementation: plans and reviews stop at recommendations and evidence limits unless implementation is requested.

Default to inspecting the relevant interface, completing the required question checkpoint, completing a verifiable batch, checking its effects, and using feedback to determine the next step. Research, direction exploration, and prototyping are optional tools; the question requirements below are mandatory. Enter research or prototyping when it resolves a material uncertainty or the user requests it. Scale depth by uncertainty, impact, and rework cost, not just page count.

For requested local fixes: reproduce → clarify the intended direction and key affected design details through distinct questions and understand the responses → identify the affected layout/state/token → make the smallest authorized change → retest the affected path and nearby regressions → report. For new designs, complete initial discovery before creating the interface. Resume settled work without restarting discovery, while meeting the checkpoint for each new change request.

Read only relevant reference sections at their point of use. Routine work can follow this entrypoint; reference examples and templates do not add deliverables to the user's request.

## Write clear user-facing output

Apply this requirement to every user-facing output produced while using this skill, including interface copy, documents and specifications, questions and options, conversational replies, progress updates, reviews, and handoffs. Do not use unnecessary defensive wording, unnecessary negation, stacked qualifiers, jargon, or confusing acronyms. State facts, actions, outcomes, and next steps directly in language the audience understands.

Use [clear-output guidance](references/interview-and-decisions.md#write-clear-user-facing-output) when drafting and reviewing these outputs; also apply the interface-specific copy guidance when authoring UI text.

## Keep the user involved

Complete these question checkpoints before the affected design or implementation, unless the explicit full-delegation exception below applies:

| Trigger | Required useful questions to the user |
| --- | --- |
| Design an interface from scratch | 8–16 total during initial discovery, before creating mockups, UI, or frontend code; cover every ambiguous requirement or design choice the user has not explicitly settled or delegated |
| Later substantially change layout | At least 2 about layout: one about direction and one about a key affected detail |
| Later substantially change motion | At least 2 about motion: one about direction and one about a key affected detail |
| Each user request to modify or fine-tune the design | At least 2 distinct questions: one about the intended direction or result and one about a key affected design detail |

When a later change substantially affects both layout and motion, ask at least 4 questions: a direction question and a key-detail question for each area. Those questions also satisfy the change-request minimum. Ask no more than 16 questions per round, counting all messages and question tools before the user's next reply. Initial discovery has an additional total cap of 16 across all rounds, including follow-ups. Split questions across rounds when answers have dependencies. At the cap, list any unresolved ambiguities and wait for the user to supply or delegate the missing decisions before creation. Use [counting and round guidance](references/interview-and-decisions.md#count-questions-and-control-each-round).

- Read the brief, existing decisions, real content, and discoverable project facts first. For work from scratch, ask about every ambiguous project need or design choice the user has not explicitly settled or delegated; keep unanswered choices pending rather than filling them with assumed preferences. A detailed brief, a small task, or plausible defaults do not waive the minimum; use known facts to explore relevant implications and tradeoffs without repeating settled answers.
- Every question must name a specific task, page, element, content item, or state and the unresolved decision it will advance. Explain how its viable answers affect requirements, design, implementation, or acceptance. Do not ask broad, empty prompts, abstract adjective preferences, repeated questions, or filler to meet the count. Apply the [question-quality guidance](references/interview-and-decisions.md#make-questions-answerable) before posing any question.
- For changes to an existing project, ask about the direction and [key design details](references/interview-and-decisions.md#clarify-direction-and-key-design-details). Cover unresolved details that affect information hierarchy, content, visual hierarchy, responsive behavior, interaction, or motion; use the actual interface and explain the user-visible consequence. Ask separate direction and detail questions, preserving settled answers and explicit delegation.
- Prefer multiple choice for design tradeoffs: normally offer 3 distinct, viable options; keep genuinely binary decisions to 2. Factual questions may accept direct input; offer choices when known alternatives make answering easier. Include a custom-answer path, explain practical differences, and recommend a design option. Never invent facts or filler options. Use relevant frontend terms with a brief explanation of their effect; see [question patterns](references/interview-and-decisions.md#use-professional-terms-to-expose-the-actual-choice).
- Prefer the host’s available native structured question tool, following its schema, allowed mode, and per-call limits. Preserve the question format above and use text only when no suitable native tool is available. Split batches within the checkpoint caps; see [native question guidance](references/interview-and-decisions.md#use-native-question-tools).
- For new interfaces and substantial redesigns, explicitly check UI language/voice and motion purpose/intensity. Include unsettled directions in the required questions, using [copy](references/interview-and-decisions.md#write-natural-interface-copy), [layout](references/interview-and-decisions.md#important-layout), or [motion](references/interview-and-decisions.md#important-motion) comparisons. Generic requests such as “modern” or “polished” do not settle these choices.
- Waive the question checkpoints only when the user explicitly delegates the entire design and implementation of the requested task to AI. Delegating a direction, individual details, or routine implementation alone does not waive them. Within full delegation, choose unresolved design preferences autonomously; still obtain indispensable facts and required permissions. Keep consequential choices visible and preserve any requested review point. Silence is not approval; liking a reference is not approval of an entire redesign.
- Unless the full-delegation exception applies, wait for answers and summarize the intended outcome, priorities, constraints, direction, and key details at an appropriate scale. Counts alone are insufficient: resolve or obtain delegation for remaining ambiguous needs and choices within the applicable cap before dependent work. Continue independent read-only inspection or research while waiting.
- After the relevant checkpoint, tune routine spacing, type sizes, timing, and other implementation parameters within the settled direction and key-detail decisions. A newly found ambiguity that changes those decisions needs clarification before affected work. Repairs against the agreed behavior do not trigger a new question quota unless they substantially change layout or motion, or the user makes a new change request.
- For difficult tradeoffs, use [answerable questions](references/interview-and-decisions.md#make-questions-answerable) and [decision boundaries](references/interview-and-decisions.md#preserve-decisions-rather-than-complete-chats). Do not ask the user to choose technical parameters without explaining their effect.

## Preserve design quality

Use user tasks, real content, and established brand facts to guide information hierarchy, typography, layout, density, color, assets, and interaction. Form a coherent visual direction appropriate to the project; do not apply one palette, grid, font pairing, or motion intensity everywhere. Label temporary material; never invent clients, statistics, testimonials, or commitments.

Explain design choices in the user's language with concrete tradeoffs. New UI content follows explicit instructions → established project language and confirmed audience → conversation language as fallback. Preserve locales and protected copy; clarify material conflicts before translating. Avoid generic promotional slogans, forced intimacy, poetic reassurance, padded politeness, and implementation commentary. Use specific actions and facts, retaining necessary context. When authoring UI text, apply [natural interface copy](references/interview-and-decisions.md#write-natural-interface-copy).

Distinguish observed behavior, source inference, design judgment, and unverified claims. Screenshots do not prove interaction, builds do not prove usability, and emulation does not prove physical-device behavior. Use [evidence guidance](references/reference-evidence.md#classify-evidence-before-using-it) for consequential claims and [sources](references/sources.md) when checking standards, attribution, or third-party reuse.

## Audit and define

Before changing an existing interface, inspect the affected pages and states in a real browser when available. Broaden to representative templates and paths for shared or sitewide changes. Capture enough version, viewport, and interaction evidence to reproduce findings. Use source code to understand ownership and constraints. Without browser access, continue permitted checks and explicitly leave rendered behavior unverified.

Identify what to preserve, the highest-impact problems, and the intended outcome. Establish relevant acceptance criteria before implementation; do not lower them afterward to conceal failures. For broad audits, consult [audit coverage](references/reference-evidence.md#audit-the-project-before-collecting-inspiration). Reuse existing briefs to make required questions specific; preserve settled facts and choices.

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
