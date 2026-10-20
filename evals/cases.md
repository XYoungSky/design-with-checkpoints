# Regression Cases

These cases are for revising the skill. They are not installed with it.

## How to run

1. Give a fresh agent the skill, one realistic request from the table, and a fixture project. Do not show it the expected behavior.
2. Allow only read-only or explicitly permitted actions. A regression run never publishes, contacts anyone, or changes a live service.
3. Keep the skill version, model, tools, prompt, and full output.
4. Judge the actual output and artifacts against the expected behavior, not against matching phrases.
5. When comparing two skill versions, use the same request, fixture, model, and tools, and hide which version produced which output from the reviewer.

One run is a signal, not proof. Repeat across several cases before claiming an improvement.

## Cases

| # | Request | Expected behavior |
| --- | --- | --- |
| 1 | New portfolio site from a vague brief | Restates the brief in 3–5 lines, asks one round of design-changing questions with options and a recommendation, including taste input, and waits; then proposes 2–3 directions as pages the user can open, with motion intensity asked separately |
| 2 | New landing page from a detailed brief | Does not re-ask settled facts; asks only about open decisions, or asks the user to confirm the restated brief; still runs the direction checkpoint |
| 3 | "The project title is clipped in the mobile nav" | Fixes it directly, shows before and after, retests 320 and 390px and the neighboring breakpoint; no discovery round |
| 4 | "Make the header lighter" | Recognizes two readings (visual weight or color) and asks one question or shows both variants |
| 5 | Replace the primary navigation | Treats it as a substantial layout change and runs checkpoint 2 for navigation |
| 6 | Add transitions to a daily-use dashboard | Assigns each animation a job and a frequency; keeps high-frequency motion at 150ms or less or removes it; delivers a motion inventory |
| 7 | "Make scrolling feel like Apple's product pages" | Explains the tradeoff, proposes native scroll-linked effects; adds scroll hijacking only if the user insists, with the purpose recorded |
| 7b | "The motion feels flat; make it richer" on a portfolio | Shows calm, lively, and expressive samples with the same content and recommends one; puts the richness in low-frequency moments, keeps hover and tabs within 150ms, and provides reduced-motion fallbacks |
| 8 | "You decide everything; build it" | Writes the brief and the chosen direction into the reply, builds, asks only for facts and permissions, and still runs both checks |
| 9 | "Handle the details" with no direction given | Keeps the direction checkpoint |
| 10 | "Show me a working sample before you expand it" | Builds and checks one slice, then waits |
| 11 | "Review the checkout and recommend changes; do not edit" | Makes no edits; delivers up to seven findings with location, what it sees, why it matters, a concrete fix, and a severity; keeps defects apart from design judgments; lists each animation's job; ends with one recommended next step |
| 12 | Chinese and English content site | Chinese letter spacing 0, body line height 1.7 or more, line length within range; both languages pass the layout check at 320px |
| 13 | "Make it more polished" | Names the most consequential observed issue and offers 2–3 concrete fixes with a recommendation; no broad taste questions |
| 14 | User shares a reference site they like | Asks which part they like, shows that part with the user's content, copies no assets, and does not treat it as approval of a redesign |
| 15 | Build passes but no browser is available | Reports rendered layout and motion as untested |
| 16 | Static screenshot of an animated reference | Does not invent timing or easing; states what needs to be tested |
| 17 | Drawer with rapid open and close, keyboard, and reduced motion | Reverses from the current position, returns focus, leaves no scroll lock or overlay behind, works with reduced motion |
| 18 | Backend-only API change | The skill does not trigger |
| 19 | Redesign an existing marketing page | Audits at 390 and 1440px first; restates the brief with a keep list and 3–5 problems tied to screenshots; changes only the agreed areas |
| 20 | Promo page; the user picks a quiet, typographic direction | Asks motion intensity as a separate question, recommends lively for a promotional page, and does not infer calm motion from the visual style |
| 21 | The user combines parts of two directions | Confirms whatever the combination leaves open, such as motion intensity or color, before building |
| 22 | "This entrance animation feels unnatural" | Replaces it with motion derived from the content at the same intensity; does not remove motion; avoids fade-up entrances and bounce |
| 23 | Sample review on a page with rich motion | Takes a few screenshots and reads the code; uses no computer use, frame sequences, or videos; gives the user the page to open with the motion inventory |
| 24 | Copy for a promotional page | At most one slogan-style headline; other headings say what the section shows |
| 25 | "动效不行" during sample review | Before editing, asks which animation and what is wrong, with 2–3 interpretations and a recommendation; restates the change in one line, then makes it |
| 26 | "改得高级一点" on an existing page | Asks which dimension carries the feeling (type, space, color, imagery) with visible effects, or shows two small variants; does not guess |
| 27 | "Make the hero heading 56px and keep the rest" | Makes the change without questions, because the element and the change are both named |
| 28 | "The toggle looks plain; find a nicer one" | Clarifies what "nicer" means and designs the toggle from the agreed direction; does not search component galleries unprompted |
| 29 | "Look at Uiverse for a toggle idea" | Gives 2–3 direct uiverse.io links with why each fits, what it would change, and a recommendation; builds no sample unless asked; after the user picks, adapts it to the project's tokens, motion rules, and accessibility and keeps the credit; says so if nothing fits |

## Hard gates

A run fails, whatever its other qualities, if it:

- invents facts, content, or test results;
- builds beyond the sample before the user approves it, without full delegation;
- delivers an animation with no stated job;
- reports a failed layout check item as passed;
- takes an external action without permission.

Record separately: unnecessary questions, rework caused by misalignment, the quality of the design proposals, machine-made patterns in the result, quoting the skill's rules to the user, and verification beyond a few screenshots and a read of the code.
