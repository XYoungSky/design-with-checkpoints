# Interview and Decisions

## Order questions by dependency

Check existing answers first. Locate the current gap across goals, content priorities, information architecture, visual/interaction direction, prototypes, and acceptance. Revisit assumptions when new evidence warrants it; do not turn stages into one-way formalities.

- If the goal is unsettled, use the actual visitor scenario to compare concrete first actions, such as finding a project, comparing a service, or booking a consultation, before asking about colors.
- If content priority is unsettled, identify a real conflict, such as whether case studies or articles should appear first.
- If structure is unsettled, compare reading order, paths, and density before decoration.
- If direction is approved, focus required questions on the requested result, preserved boundaries, and affected typography, layouts, or interactions; keep unrelated decisions settled.
- If the solution is established, make the direction and key-detail questions specific to its intended result, preservation boundaries, or acceptance conditions, then handle routine parameters within those answers.

Apply the [required question checkpoints and full-delegation exception](../SKILL.md#keep-the-user-involved). In initial discovery, cover actual gaps in audience, primary task/outcome, content priority, language/voice, layout, motion, key details, constraints, and acceptance. Use a detailed brief to explore implications without repeating known facts. Ask prerequisite questions first and synthesize conflicting feedback before proposing the next choice.

## Clarify direction and key design details

Use the [change-request checkpoint](../SKILL.md#keep-the-user-involved): direction sets the desired outcome; key details determine how users experience it. Cover remaining consequential detail choices using the existing interface and content.

Key details can include which content gets emphasis, how long titles are shown, what remains visible on mobile, which component states need feedback, how errors are recovered, and when motion occurs during repeated use. Ask about the visible behavior and its tradeoffs. Routine pixel values, library choices, and tuning follow the settled decisions. Preserve explicit answers and delegated details; use the questions to resolve actual remaining choices, constraints, or acceptance conditions.

## Count questions and control each round

Count questions actually posed to the user for the current stage or change request. The minimum counts distinct, answerable decisions; repeated or reworded questions consume the upper limit without helping meet the minimum. Options and the custom-answer entry belong to one question; they do not count separately. Explanations and recommendations do not count as questions. If a numbered item requests several independent answers, count each separately; grouping them under one heading does not bypass the cap. Direction and key-detail questions must be distinct. A question can meet the general change requirement and the corresponding layout or motion requirement; one layout question cannot also count as a motion question.

Use the round and initial-discovery caps in [the checkpoint rules](../SKILL.md#keep-the-user-involved). Split dependent questions across rounds; do not split tools or restart discovery to reset the count. Repeated questions and follow-ups consume the applicable cap. Do not add filler to reach the minimum.

A substantial layout change alters information order, page structure, navigation, the main composition, or density enough to affect reading or task completion. A substantial motion change alters purpose, intensity, choreography, scroll behavior, or repeated-use experience. Apply the corresponding minima in [the checkpoint rules](../SKILL.md#keep-the-user-involved), including separate direction and detail questions for both areas when both change.

After answers, briefly connect the user's needs to the next action and retain material unresolved questions. Do not begin dependent work while required responses or material understanding are missing. Counting questions is a guard against premature creation, not evidence that the needs are understood.

## Make questions answerable

Check every question before presenting it: name the actual task, page, element, content, or state; identify one unresolved decision; and explain how its answers affect the next requirement, design choice, implementation, or acceptance check. Ground it in the brief or observed interface. When facts are missing, ask about specific relevant scenarios rather than inventing evidence. Reject broad prompts such as “What style do you like?” or “What should we improve?” and questions whose answers would leave the next step unchanged.

Use the [question-format rule](../SKILL.md#keep-the-user-involved): prefer choices for design tradeoffs, retain two for binary decisions, and allow direct input for facts. Alternatives should differ in a relevant outcome, priority, scope, or condition. Accept custom answers and added constraints; resolve conflicts before dependent work.

Examples of grounding a question; verify the scenario and provide the full options, effects, recommendation, and custom-answer path when presenting it:

| Avoid | Specific decision to resolve |
| --- | --- |
| “What style do you like?” | For a service homepage with supplied case studies, compare opening with a representative case, service and booking information, or a short introduction followed by case previews; explain the visitor's first action in each. |
| “How should we improve the cards?” | For a mobile project list with clipped titles, compare full-title wrapping, a summary linked to the full title, or an expandable title; explain reading completeness, list density, and extra interaction. |

Use natural language to include the relevant elements below; do not dump every template field into the chat.

1. Evidence: “The homepage has 12 projects; three demonstrate the primary service most clearly.”
2. Decision: “How should the homepage order the three selected projects and the full 12-project index for new visitors?”
3. Recommendation and reason: “I recommend selected projects first so new visitors can understand the work.”
4. Three choices and costs: “A. Selected projects with a separate index: clearer introduction, with another step to find unfeatured work. B. Faceted index first: faster targeted browsing, with more category choices upfront. C. Selected projects followed by the full index on the same page: supports both paths, with a longer homepage.”
5. Comparison: “All three use the same projects and images and work on mobile.”
6. Boundary: “This chooses the homepage order, without changing detail-page content.”

Avoid loaded pseudo-options such as “premium/basic” or “professional/playful.” Keep all options viable and explain their differences without declaring alternatives inferior. The custom-answer path is separate from the substantive options.

## Use native question tools

Inspect the question capabilities actually exposed in the current session. Prefer Codex's or Claude Code's native structured user-question tool when it can present the required choices. Follow its current schema, mode restrictions, and per-call limits; do not invent a tool name or call a mode-restricted tool outside its supported mode.

Supply options or direct factual input according to the question-format rule, with short labels and concise descriptions when supported. For design choices, mark the recommendation using the tool's supported convention, placing it first when expected. If the UI already provides custom/free-text input, use that entry and do not duplicate it as an option. If custom input must arrive in chat, explicitly invite a custom reply alongside the native question. A preselected recommendation is not a submitted answer.

When a suitable native tool is unavailable or cannot preserve the format, present the appropriate choices or factual input in text. For choices, explain their effects, recommend a design option, and invite a custom answer. If a tool's per-call question limit is lower than a checkpoint minimum, split the batch into permitted calls or successive rounds. Respect the checkpoint caps across calls and rounds. Changing presentation does not waive question quality, counts, or the need to wait for answers.

## Use professional terms to expose the actual choice

Write the following patterns in the user's language. Use the established local term first; retain an English term or API name only when it clarifies implementation. Briefly explain its visible or operational consequence. The user chooses the outcome and important tradeoff; the assistant owns routine parameter tuning within that choice.

- Information architecture: “A. Selected-case landing with a secondary project index. It establishes the main story first; finding an unfeatured project adds a navigation step. B. Faceted project index. It exposes the whole collection immediately; categories and empty-result recovery need stronger design. C. Selected cases followed by an index on the same page. It supports both entry paths but increases page length.”
- Layout: “A. Asymmetric grid with a dominant content column. It establishes hierarchy through relative width. B. Equal-width modular grid. It supports peer-item comparison with less emphasis on any one item. C. Full-width editorial rows. They support sequential reading, with more scrolling and less side-by-side comparison.” State actual columns, content, and mobile reflow in the comparison.
- Typography: “A. Display/body role separation with a larger type-scale contrast. It makes headings more prominent but increases wrapping risk. B. A compact hierarchy with smaller size steps. It fits dense screens but needs clearer weight and spacing differences. C. Editorial hierarchy with section labels and restrained display text. It supports sustained reading but gives the opening headline less prominence.” Show real text, including all supported scripts.
- Interaction: “A. Inline disclosure. Context stays visible, but the page grows. B. Modal dialog. It isolates a short task, but requires intentional focus entry, containment, and restoration. C. A dedicated detail page. It provides room for a longer task but adds navigation and requires a clear return path.” Do not recommend a modal only because it looks cleaner.
- Motion: “A. Direct state change. Immediate access with minimal movement. B. Short spatial transition. It explains where the panel came from; it needs interruption, reversal, and reduced-motion behavior. C. Motion selected by context. Frequent actions change directly while occasional orientation moments use a short transition; this needs clear, consistent trigger rules.” Show relevant behavior at normal speed. Discuss duration, easing, and displacement as testable implementation parameters, not taste quizzes.

Compact question pattern: **Decision and evidence → A/B/C mechanisms and tradeoffs → recommendation → custom-answer invitation → what this approves → next test.** Include only the pieces needed to answer; adapt the options to binary decisions and use direct input for facts when appropriate. Select the batch using the checkpoint minimum and round cap. Mark recommendations without calling alternatives inferior by definition.

For a substantial final plan, name information architecture, semantic tokens, type hierarchy, grid/gutters, responsive rules, component states, focus management, motion choreography, and acceptance tests accurately. Pair each consequential technical statement with a practical implication. For a narrow fix, name only the affected mechanisms. Use the [frontend specification](project-templates.md#frontend-specification); do not produce a vocabulary list in place of a design.

State the UI language and content-design rule in the plan, following the language priority in [the skill](../SKILL.md). The discussion language may differ from the interface language. Preserve established localization and protected copy. Describe design tradeoffs precisely in specifications; write interface text for its audience, with clear actions, useful recovery messages, and necessary context at the point of use.

## Write clear user-facing output

Apply the skill's [clear-output rule](../SKILL.md#write-clear-user-facing-output) to documents and conversation as well as interface text.

- Lead with the fact, result, recommendation, or action. Remove preemptive self-justification and unprompted contrasts or denials that do not help the reader understand or act.
- Keep qualifications only when they affect accuracy, a decision, or the next action. State concrete conditions once, near the relevant claim, and separate independent conditions into readable sentences. Preserve actual uncertainty, access restrictions, meaningful consequences, and required information.
- Replace buzzwords and internal shorthand with familiar words. When precision requires a technical term or abbreviation, explain its meaning or practical effect on first use unless it is already established for that audience.

## Write natural interface copy

For new interfaces or substantial changes to voice, inspect the brief, audience, and existing copy first. When voice remains unsettled and not delegated, ask the user to compare three short versions of the same real heading, action, or status message, with a recommendation and the practical differences in tone; also allow a custom rewrite. Include this in the relevant required checkpoint. Follow the skill's language priority; distinguish interface language from voice. “Use natural copy” guides quality but does not settle brand personality. After the choice, apply it across relevant labels and states; routine wording edits stay within the established voice and use the change-request checkpoint.

Write text that belongs in the product and sounds natural to its audience. Avoid empty superlatives, generic promises, forced intimacy, poetic reassurance, and long courtesy formulas around simple actions. Keep implementation reports and explanations of the design process out of the interface. Explain access restrictions, consequences, and recovery steps where they help users act; preserve necessary consent, security, and legal information.

Prefer a specific action, object, or state. Describe errors using known facts and a useful next step; do not invent a cause to make the message sound helpful. Judge phrases in context rather than maintaining a blacklist of individual words. Brand personality can shape the voice while labels and instructions remain clear.

Illustrative rewrites; adapt them to the actual behavior and locale:

| Context | Avoid | Prefer |
| --- | --- | --- |
| Project navigation | “开启灵感之旅，探索无限可能” | “查看项目” |
| Empty saved-items list | “这里静候着与你的美好相遇” | “还没有收藏” |
| Save confirmation | “We're delighted to let you know your changes have been successfully saved!” | “Changes saved.” |
| Failed upload, cause unknown | “Oops! A little hiccup interrupted your journey.” | “Upload failed. Try again.” |

## Adapt questions to the project

Use the following as question-building examples, not a universal questionnaire or default recommendations. Replace assumptions with verified project facts.

### Portfolio or case-study site

For first-time visitors, compare a small narrative-led selection with an index-first layout. The former controls emphasis; the latter supports quick filtering. Test first-glance hierarchy with the same work and assets.

To explore personal character, show two typography samples using real headings and body text in the project's supported languages. Explain tradeoffs among distinctiveness, long-form reading, font loading, and mobile wrapping. Do not ask the user to choose font names in isolation.

### Frequently used product interface

Establish frequent tasks and information volume. Compare a dense overview with progressive disclosure. The former reduces clicks but requires clearer scanning; the latter reduces initial load but may increase repeated-operation cost. Recommend after testing the same task and data.

Do not transfer generous whitespace or slow transitions from a reference into a daily-use console without justification. Ask the user to choose information tradeoffs and behavior patterns, not a spring parameter.

### Content or knowledge site

Compare topic-led discovery with direct search/index access against actual reading paths. Demonstrate long titles, hierarchical navigation, and continuous prose. Test whether users can locate information and sustain reading. Do not invent empty categories to make a small content collection seem richer.

### Marketing or service site

Ask what evidence visitors need before acting. Use available material to compare case-study-first, product-explanation-first, or problem-and-promise-first structures. Explain their effects on comprehension and credibility. Never fill missing proof with invented statistics.

### Important layout

Before a substantial layout adjustment, ask at least two questions: one about layout direction and one about a key affected detail. Use real content to clarify, for example, which information or action should gain priority, then how long titles, card density, navigation, or mobile reordering should behave. Compare the practical effects of viable structures and recommend one; do not ask for a column count without explaining the experience. Preserve unrelated approved choices.

### Important motion

Before a substantial motion adjustment, ask at least two questions: one about motion direction and one about a key affected detail. Clarify the purpose of movement using the same operation: direct feedback, a short spatial transition, or a more narrative candidate only when useful. Then resolve a concrete detail such as which repeated actions animate or when the control becomes usable during the transition. Describe or show the visible difference, explain perceived waiting, orientation, and mobile impact, and recommend a project-appropriate starting point. For initial design, include unresolved motion needs in discovery. Ask about the experience, not a duration, easing curve, or library. Refine parameters through samples after the checkpoint is complete. Do not equate more animation with better design.

## Preserve decisions rather than complete chats

Preserve high-impact decisions in existing records or a concise handoff: the choice, rationale, approval or delegation scope, and unresolved consequences. Add alternatives, evidence links, or IDs only when useful for later work; do not create a separate record for routine adjustments. Preserve the user's exact intent and the source; do not broaden praise into approval.

- “I like this font” records feedback on a font candidate, not approval of a sitewide redesign.
- “Use A's structure and B's heading treatment” approves those specific parts; check compatibility.
- “The preview is fine” may answer a clear acceptance request, but does not by itself grant new permission to publish.
- “You decide the details” delegates details; “Choose the direction and implement it” delegates direction and implementation. Neither alone delegates the entire design task or waives question counts. “I delegate the entire design and implementation to AI; make all design decisions” explicitly grants full delegation and activates the [checkpoint exception](../SKILL.md#keep-the-user-involved). Record its scope. No design delegation expands external-action permissions.

Infer the user's desired involvement from their instructions; do not require a separate mode-selection question. A request to review a sample before expansion remains a checkpoint even when details are delegated. Reopen a settled choice only when new evidence materially changes its tradeoffs, and explain that change.

Use simple statuses: pending choice, approved, awaiting validation, or superseded. Preserve the reason when one decision replaces another so discarded directions do not return unnoticed. Keep unanswered consequential questions pending; never treat a timeout as consent.

## Take the shortest feedback loop

Apply the [change-request checkpoint and its exception](../SKILL.md#keep-the-user-involved). Inspect and reproduce independently while waiting, then take the shortest affected loop once the required answers clarify direction and key details. Do not restart initial discovery for a routine revision or ask again for parameters already delegated.

- Implementation defect: repair against the approved version and retest without restarting the interview.
- Local adjustment: combine related feedback into a comparable preview without requiring pixel-by-pixel approval.
- Direction change: explain affected scope, effort, and concrete alternatives; reopen only relevant decisions.
- New scope: clarify added pages, features, external services, or public targets before acting under the applicable authorization.

If “make it more designed” remains vague, identify the current page's most consequential issue and offer three viable approaches with their practical differences, plus a custom-answer path. If feedback conflicts, state the conflict directly, such as “make it denser” versus “give each project a full screen,” and frame three meaningful priority or conditional choices for the next round.
