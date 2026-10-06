# Interview and Decisions

## Order questions by dependency

Check existing answers first. Locate the current gap across goals, content priorities, information architecture, visual/interaction direction, prototypes, and acceptance. Revisit assumptions when new evidence warrants it; do not turn stages into one-way formalities.

- If the goal is unsettled, ask what visitors should accomplish before asking about colors.
- If content priority is unsettled, identify a real conflict, such as whether case studies or articles should appear first.
- If structure is unsettled, compare reading order, paths, and density before decoration.
- If direction is approved, ask only about typography character, key layouts, or major interactions that could still change it.
- If the solution is established, handle consistency and small fixes yourself rather than asking the user to choose every parameter.

Ask only when an unresolved, non-delegated choice changes the next step. Usually ask 1–3 questions per round whose prerequisites are already available. If one answer changes the remaining options, ask that question alone first. Synthesize conflicting feedback before proposing the smallest new choice; a clear brief may need no questions.

## Make questions answerable

Use natural language to include the relevant elements below; do not dump every template field into the chat.

1. Evidence: “The homepage has 12 projects; three demonstrate the primary service most clearly.”
2. Decision: “Should visitors see selected projects first or immediately filter the full index?”
3. Recommendation and reason: “I recommend selected projects first so new visitors can understand the work.”
4. Viable alternative and cost: “An index-first layout helps visitors with a specific goal, but needs stronger category labels.”
5. Comparison: “Both versions use the same projects and images and work on mobile.”
6. Boundary: “This chooses the homepage order, without changing detail-page content.”

Avoid loaded pseudo-options such as “premium/basic” or “professional/playful.” Do not add an unsuitable third option to fill a quota. Allow a bounded combination or an additional constraint; explain and resolve conflicts before implementing it.

## Use professional terms to expose the actual choice

Write the following patterns in the user's language. Use the established local term first; retain an English term or API name only when it clarifies implementation. Briefly explain its visible or operational consequence. The user chooses the outcome and important tradeoff; the assistant owns routine parameter tuning within that choice.

- Information architecture: “A. Selected-case landing with a secondary project index. It establishes the main story first; finding an unfeatured project adds a navigation step. B. Faceted project index. It exposes the whole collection immediately; categories and empty-result recovery need stronger design.”
- Layout: “A. Asymmetric grid with a dominant content column. It establishes hierarchy through relative width. B. Equal-width modular grid. It supports peer-item comparison with less emphasis on any one item.” State actual columns, content, and mobile reflow in the comparison.
- Typography: “A. Display/body role separation with a larger type-scale contrast. It makes headings more prominent but increases wrapping risk. B. A compact hierarchy with smaller size steps. It fits dense screens but needs clearer weight and spacing differences.” Show real text, including all supported scripts.
- Interaction: “A. Inline disclosure. Context stays visible, but the page grows. B. Modal dialog. It isolates a short task, but requires intentional focus entry, containment, and restoration.” Do not recommend a modal only because it looks cleaner.
- Motion: “A. Direct state change. Immediate access with minimal movement. B. Short spatial transition. It explains where the panel came from; it needs interruption, reversal, and reduced-motion behavior.” Show both at normal speed. Discuss duration, easing, and displacement as testable implementation parameters, not taste quizzes.

Compact question pattern: **Decision and evidence → A/B mechanisms and tradeoffs → recommendation → what this approves → next test.** Include only the pieces needed for the next answer, normally one short question with 2–3 viable options. Mark recommendations without calling alternatives inferior by definition.

For a substantial final plan, name information architecture, semantic tokens, type hierarchy, grid/gutters, responsive rules, component states, focus management, motion choreography, and acceptance tests accurately. Pair each consequential technical statement with a practical implication. For a narrow fix, name only the affected mechanisms. Use the [frontend specification](project-templates.md#frontend-specification); do not produce a vocabulary list in place of a design.

State the UI language and content-design rule in the plan, following the language priority in [the skill](../SKILL.md). The discussion language may differ from the interface language. Preserve established localization and protected copy. Describe design tradeoffs precisely in specifications; write interface text for its audience, with clear actions, useful recovery messages, and necessary context at the point of use.

## Write natural interface copy

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

### Important motion

Show direct feedback and a noticeable state transition for the same operation; add a more narrative candidate only when useful. Explain frequency, perceived waiting, orientation, and mobile cost. Recommend a project-appropriate starting point, then refine it through samples. Do not equate more animation with better design.

## Preserve decisions rather than complete chats

Preserve high-impact decisions in existing records or a concise handoff: the choice, rationale, approval or delegation scope, and unresolved consequences. Add alternatives, evidence links, or IDs only when useful for later work; do not create a separate record for routine adjustments. Preserve the user's exact intent and the source; do not broaden praise into approval.

- “I like this font” records feedback on a font candidate, not approval of a sitewide redesign.
- “Use A's structure and B's heading treatment” approves those specific parts; check compatibility.
- “The preview is fine” may answer a clear acceptance request, but does not by itself grant new permission to publish.
- “You decide the details” delegates details within approved scope. “Choose the direction and implement it” also delegates that direction choice; record the recommendation and proceed. Neither instruction expands the task's scope or external-action permissions.

Infer the user's desired involvement from their instructions; do not require a separate mode-selection question. A request to review a sample before expansion remains a checkpoint even when details are delegated. Reopen a settled choice only when new evidence materially changes its tradeoffs, and explain that change.

Use simple statuses: pending choice, approved, awaiting validation, or superseded. Preserve the reason when one decision replaces another so discarded directions do not return unnoticed. Keep unanswered consequential questions pending; never treat a timeout as consent.

## Take the shortest feedback loop

- Implementation defect: repair against the approved version and retest without restarting the interview.
- Local adjustment: combine related feedback into a comparable preview without requiring pixel-by-pixel approval.
- Direction change: explain affected scope, effort, and concrete alternatives; reopen only relevant decisions.
- New scope: clarify added pages, features, external services, or public targets before acting under the applicable authorization.

If “make it more designed” remains vague, identify the current page's most consequential issue and propose two specific changes. If feedback conflicts, state the conflict directly, such as “make it denser” versus “give each project a full screen,” and ask which priority should govern this round.
