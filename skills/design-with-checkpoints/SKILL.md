---
name: design-with-checkpoints
description: "Build new websites, redesign existing interfaces, and review frontend designs with the user at three checkpoints: an aligned brief, a chosen visual direction, and a reviewed sample. Makes opinionated layout, typography, and motion proposals, avoids machine-made patterns, and checks every layout and animation before delivery. Use for new pages, redesigns, design reviews, layout or motion changes, and visual polish; not for backend-only work."
---

# Design with Checkpoints

Build the interface the user has in mind, with a clear design point of view, and deliver only layouts and motion that pass explicit checks. Keep the process light: show concrete samples early and ask only questions whose answers change the design.

## Principles

1. **Show, then ask.** People judge layout and motion better from a page they can open than from a description.
2. **Have a point of view.** Every proposal states its idea in one sentence, names its layout, type, and motion moves, states its cost, and ends with a recommendation.
3. **Rich where it counts, reasonable everywhere.** Layouts fit their content. Motion comes from what the content does, is expressive at rare moments, and stays quick on frequent actions. Every animation has a job.
4. **Nothing machine-made.** Remove the [layout tells](references/layout-and-type.md#template-tells) and [motion tells](references/motion.md#derive-motion-from-the-content) before showing anything.
5. **Use real content and facts.** Label placeholders. Never invent clients, numbers, testimonials, or test results.

## Choose the path

Read the project first: the brief, code, existing design conventions, real content, and earlier decisions. Find out what you can yourself before asking. If other design skills are loaded, use them for research or tooling only; the direction comes from this project's content and the user's answers.

| Request | Path |
| --- | --- |
| Build a new site or page | [New site](#new-site) |
| Change the design of an existing interface | [Redesign](#redesign) |
| Assess a design without changing it | [Review](#review) |
| A local fix or tweak | [Clarify](#clarify-before-changing) anything vague, then make the change, show before and after, and check the affected widths |

## Clarify before changing

Before acting on any change request or feedback, look for points the user left vague that would change the result:

- a quality word with several meanings, such as "更高级", "不自然", or "more polished";
- an unclear scope: which page, section, element, or state;
- an unclear degree: how much bigger, quieter, or richer;
- replace or remove;
- a conflict with an earlier decision.

If any exists, ask 1–3 questions before editing. Each question quotes the user's words, offers 2–3 interpretations with their visible effect, recommends one, and accepts a custom answer. Then restate the change in one line and make it. When unsure whether a point is vague, ask one question rather than guess.

Skip this when the request names both the element and the change, when it fixes a defect against the agreed design, or when the user asked you to decide. Common vague requests and what to ask: [clarify a change request](references/alignment.md#clarify-a-change-request).

## New site

**Checkpoint 1 — Align the brief.** Restate the request in 3–5 lines: audience, primary task, available content, constraints, and what success looks like. List the open design decisions. Ask one round of questions about them, usually 3–6, including [taste input](references/alignment.md#get-taste-input) when the user has not given any. Each question offers 2–3 concrete options with their visible effect, marks a recommendation, and accepts a custom answer; use the host's native question tool when available. If the brief already settles everything, ask the user to confirm the restatement. Wait for the answers.

**Checkpoint 2 — Choose a direction.** Propose 2–3 directions that differ in a real mechanism: information order, composition, density, or type hierarchy. Color alone is not a direction. For each, give a name that explains the difference, the design idea in one sentence, its layout and type moves, what it gains and gives up, and a page the user can open with the real content at desktop and mobile width. Ask about [motion intensity](references/motion.md#choose-an-intensity) as a separate choice, with a draft [motion inventory](references/motion.md#motion-inventory); marketing pages start at lively. Recommend one direction. When the user combines directions, confirm whatever the combination leaves open before building.

**Checkpoint 3 — Review a sample.** Build one representative slice with real content and its motion, such as the first screen plus one key section. Run the layout check, give the user the page with its full motion inventory, and wait before repeating the pattern across pages.

Build proposals from [layout and type](references/layout-and-type.md) and [motion](references/motion.md); phrase questions with [alignment](references/alignment.md).

## Redesign

1. **Audit first.** Screenshot the current interface at 390 and 1440px and read its code. List what to keep (identity, content, working interactions) and the 3–5 problems that matter most, each tied to a screenshot. Note template tells, and each existing animation's job.
2. **Checkpoint 1.** Restate the brief together with the keep list and the problems, then ask about the open decisions.
3. **Checkpoint 2** only for the areas that change. Everything on the keep list stays as it is.
4. **Checkpoint 3** when the change spans several pages.

Preserve content, URLs, and working behavior unless the user asks to change them.

## Review

Make no edits. Screenshot the interface at 390 and 1440px, read its code, and deliver:

- up to seven findings, most important first, each with where it occurs (page, width, state), what you see, why it matters to the visitor, a concrete fix with values, and a severity: blocker, important, or polish;
- defects (broken, unreadable, inaccessible) kept apart from design judgments (hierarchy, rhythm, machine-made patterns), labelled as such;
- a short motion section: each animation's job, and the ones without one;
- one recommended next step, with an offer to make the changes.

## Build

Work in coherent batches within the existing stack and components; add a library only when the task needs it. Design components from the agreed direction; look at outside component galleries only when the user asks, following [outside galleries](references/layout-and-type.md#outside-component-galleries). Tune spacing, sizes, and timing yourself within the agreed direction, and return to the user only when a new question would change that direction. Record each consequential decision as one line: the decision, the reason, and who approved it.

## Check before delivery

- **Layout check.** Every changed page passes the [layout check](references/layout-and-type.md#layout-check).
- **Motion inventory.** Every animation has a row with a stated job. Remove animations that have none, and include the final inventory in the report.
- **Light verification.** Follow [verify](references/verify.md): a few screenshots and a read of the code. No computer use, frame captures, or videos; the user judges motion on the live page.

## Delegation

When the user explicitly hands over the whole design, for example "you decide everything", skip the waits at checkpoints 1 and 2: write the brief and the chosen direction with its reasons into your reply, then build. Still ask for facts only the user has, such as content or permissions, keep any review point the user asked for, and run all checks.

"Handle the details" delegates details only. The direction checkpoint stays.

## Feedback

Clarify vague points first, as above. Then:

- Defect against the agreed design: fix it and retest.
- Criticism of a specific element or animation ("this motion feels wrong"): replace it with one that fits the content better at the same intensity. Remove or tone down only when the user says so.
- Local adjustment: group related feedback and show before and after.
- Direction change: explain what it affects, then return to checkpoint 2 for that area only.

Liking a reference or a font is feedback on that item, not approval of a redesign. Silence is not approval.

## Communication

Write to the user in their language and talk about the design, not the process. Do not quote or cite this skill's rules to the user; ask the question directly. Lead with the result or recommendation, and explain design terms by their visible effect. Interface copy follows the project's language and voice; see [interface copy](references/alignment.md#interface-copy).

## Stop

Stop when the requested deliverable and its checks are complete, or at a decision only the user can make. Report what changed, what you checked, and what remains untested.
