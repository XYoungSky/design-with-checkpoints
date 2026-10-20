---
name: design-with-checkpoints
description: "Design, redesign, and review websites and frontend interfaces with the user at three checkpoints: an aligned brief, a chosen visual direction, and a reviewed sample. Makes opinionated layout, typography, and motion proposals, and checks every layout and animation before delivery. Use for new pages, redesigns, layout or motion changes, and visual polish; not for backend-only work."
---

# Design with Checkpoints

Build the interface the user has in mind, with a clear design point of view, and deliver only layouts and motion that pass explicit checks. Keep the process light: show concrete samples early and ask only questions whose answers change the design.

## Principles

1. **Show, then ask.** People judge layout and motion better from a sample than from a description.
2. **Have a point of view.** Every proposal states its idea in one sentence, names its layout, type, and motion moves, states its cost, and ends with a recommendation.
3. **Rich where it counts, reasonable everywhere.** Layouts fit their content. Motion can be expressive at rare moments such as a first view or a section entrance, and stays quick on frequent actions. Every animation has a job. Check both before delivery.
4. **Use real content and facts.** Label placeholders. Never invent clients, numbers, testimonials, or test results.
5. **Scale to the task.** A one-line fix gets a fix, not a discovery round.

## Route the task

Read the project first: the brief, code, existing design conventions, real content, and earlier decisions. Find out what you can yourself before asking.

| Request | Path |
| --- | --- |
| New interface or redesign | Checkpoints 1 → 2 → 3, then build |
| Substantial layout or motion change: reading order, page structure, navigation, density, or the purpose and intensity of motion | Checkpoint 2 for the affected area; add checkpoint 3 when the change spans pages |
| Clear local fix or tweak | Make the change, show before and after, retest the affected path. Ask one question only when two reasonable readings would look visibly different |
| Plan or review only | Deliver findings and recommendations; stop before implementation |

## Checkpoint 1 — Align the brief

Restate the request in 3–5 lines: audience, primary task, available content, constraints, and what success looks like. List the open design decisions. Then ask one round of questions about the decisions the brief leaves open, usually 3–6 for a new interface. Each question offers 2–3 concrete options with their visible effect, marks a recommendation, and accepts a custom answer. Use the host's native question tool when one is available. If the brief already settles every decision, ask the user to confirm the restatement instead. Wait for the answers before designing.

How to choose and phrase questions: [alignment](references/alignment.md).

## Checkpoint 2 — Choose a direction

Propose 2–3 directions that differ in a real mechanism: information order, composition, density, type hierarchy, or motion approach. Color alone is not a direction. For each direction give:

- a name that explains the difference, and the design idea in one sentence;
- the layout, type, and motion moves that realize it, including the motion intensity (calm, lively, or expressive) and a draft [motion inventory](references/motion.md#motion-inventory) of what will move;
- what it gains and what it gives up;
- a quick sample with the real content: the first screen at desktop and mobile width, with motion shown at normal speed when motion is part of the choice.

Recommend one and explain why in terms of the user's goal. The user can pick one, combine parts, or redirect. When the direction is already settled, go to checkpoint 3.

Build proposals from [layout and type](references/layout-and-type.md) and [motion](references/motion.md).

## Checkpoint 3 — Review a sample

Build one representative slice with real content and its motion, such as the first screen plus one key section, or one component with all its states. Run the layout check on it, show it together with its full motion inventory, and wait for the user before repeating the pattern across pages.

## Build

Work in coherent batches within the existing stack and components; add a library only when the task needs it. Tune spacing, sizes, and timing yourself within the agreed direction, and return to the user only when a new question would change that direction. Record each consequential decision as one line: the decision, the reason, and who approved it.

## Check before delivery

- **Layout check.** Every changed page and state passes the [layout check](references/layout-and-type.md#layout-check).
- **Motion inventory.** Every animation has a row in the [motion inventory](references/motion.md#motion-inventory) with a stated purpose. Remove animations that have none, and include the final inventory in the report.
- **Verification.** Follow [verify](references/verify.md): screenshots at the listed widths, keyboard and reduced-motion passes, and a report that separates what you observed from what you could not test.

## Delegation

When the user explicitly hands over the whole design, for example "you decide everything", skip the waits at checkpoints 1 and 2: write the brief and the chosen direction with its reasons into your reply, then build. Still ask for facts only the user has, such as content or permissions, keep any review point the user asked for, and run all checks.

"Handle the details" delegates details only. The direction checkpoint stays.

## Feedback

- Defect against the agreed design: fix it and retest.
- Local adjustment: group related feedback and show before and after.
- Direction change: explain what it affects, then return to checkpoint 2 for that area only.
- Vague feedback such as "make it more polished": name the most consequential issue you see and offer 2–3 concrete fixes with a recommendation.

Liking a reference or a font is feedback on that item, not approval of a redesign. Silence is not approval.

## Communication

Write to the user in their language. Lead with the result or recommendation, and explain design terms by their visible effect. Interface copy follows the project's language and voice; see [interface copy](references/alignment.md#interface-copy).

## Stop

Stop when the requested deliverable and its checks are complete, or at a decision only the user can make. Report what changed, what you checked, and what remains untested.
