# Project Templates

Contents: [brief](#brief-and-working-boundaries) · [traceability](#requirements-to-tests) · [evidence](#audit-or-reference-card) · [decisions](#decision-record) · [experiments](#prototype-experiment) · [frontend specification](#frontend-specification) · [feedback](#defect-and-feedback-batch) · [handoff](#acceptance-and-handoff) · [skill evaluation](#skill-regression-evaluation).

Preserve only what helps work continue. Prefer the project's existing design records or agreed location; create a short record only when needed. Use the relevant fragments within one existing record; do not create a separate document for each template. A small change can be covered by its final handoff. Omit unused fields, formal IDs, and publishing details when they do not help the task. Link screenshots and recordings to identifiable versions so conclusions remain reviewable.

## Brief and working boundaries

- Target site/project, current version, specified environment:
- Primary audience and main task:
- Real content, content priorities, brand/asset sources:
- Scope, preserved elements, protected elements:
- Technical, time, and asset constraints; unknowns:
- Acceptance criteria and stopping conditions:
- Preview mode, address, and visibility:
- Publishing target, existing authorization, outstanding confirmations:
- Change batch and rollback method:

Label unknowns as pending confirmation or testing. Do not convert assumptions into facts or describe planned work as completed without evidence.

## Requirements to tests

For consequential requirements that need tracking across decisions, implementation, or handoffs, use the relevant fields below. A short explanation suffices for a simple change; IDs are optional:

- Requirement ID, user task/outcome, source, priority, and constraint.
- Baseline/evidence; normative requirement, measured observation, heuristic, or proposed hypothesis.
- Decision ID, considered mechanisms, rationale, approval scope/status.
- Implementation location: route, component, semantic token, or state transition.
- Test ID: setup/input, observable expected result, threshold or failure condition, method.
- Actual result and evidence for an identified version: passed, failed, or untested; remaining risk.

Example, not a universal target: R-01 “Users can reopen the filter without losing their selection” → D-01 “Preserve filter state across panel visibility changes” → FilterPanel state model → T-01 “Choose a filter; close/reopen by pointer and keyboard; the same selection, results, and accessible state remain; after dismissal focus returns to the trigger.” Test rapid reversal and reduced motion separately. Approval of D-01 does not mean T-01 passed.

Acceptance statements should identify condition + behavior + evidence. Replace “mobile-friendly” with a named path at specified widths and inputs, no unintended overflow, and intact content/controls. Replace “smooth animation” with correct interruption/final state plus a defined performance measurement. Set thresholds before running; if a threshold changes, record why and retest rather than rewriting a failure as a pass.

## Audit or reference card

- ID and type: current-site finding or external reference.
- URL, page/state, version, inspection date:
- Browser, viewport, input method, inspection method:
- Screenshot, recording, interaction, or source-code evidence:
- Actual observation:
- Inference and supporting grounds:
- Effect on the project task or transferable mechanism:
- Elements to preserve or avoid copying:
- Specific recommendation, alternatives, and costs:
- Asset/code usage rights:
- Unverified items, priority, and validation method:

## Decision record

- Decision ID, question, downstream effects:
- Known facts and supporting evidence:
- Alternatives and differences; recommendation and reason:
- Comparison samples using the same content:
- User choice, source/time, exact approval scope:
- Details delegated for autonomous adjustment:
- Open questions and next validation:
- Status: pending choice, approved, awaiting validation, or superseded.
- Superseded decision and reason for change:

## Prototype experiment

- Hypothesis and user task:
- Variables changed and conditions held constant:
- Desktop and mobile prototypes/versions:
- Observation method and failure condition:
- Actual results, user feedback, untested parts:
- Conclusion: adopt, revise and retest, or reject; applicability:
- Participants/reviewer type, task prompt, assistance, errors, completion count/denominator:
- Time/action-count method if relevant; confounds, sample limits, and uncertainty:

## Frontend specification

Use this when a specification is requested or needed for complex behavior, cross-page coordination, or handoff. Reuse existing design and code records; document new agreements without transcribing unchanged implementation. Localize its professional terminology to the user's language; explain the consequence of important choices briefly. Include only relevant sections, and link to detailed evidence instead of dumping every token into chat.

1. **Outcome and information architecture:** target audience/task, entry points, content priority, navigation, page/template hierarchy, and the critical path. Link decisions to requirements and preserve approved copy.
2. **Design tokens and visual hierarchy:** reuse existing primitive and semantic tokens. Specify role → token → value/unit or existing source, including surface/text/action/feedback colors, spacing, typography, borders, radii, elevation, and motion only where used. Keep semantic roles separate from raw values so a palette change does not erase error/success/warning distinctions. Document component overrides and exceptions. Use the [DTCG format](https://www.designtokens.org/tr/2025.10/format/) only when token interchange benefits this project; it is a Community Group specification, not a required W3C Recommendation or an instruction to migrate tools.
3. **Typography:** display/heading/body/label/data roles; family and licensed source, language coverage, fallback stack, size, weight, line height, tracking, and responsive behavior. Specify actual project values or bounded formulas after samples; distinguish proposals from approved values. Test heading wraps, long strings, mixed scripts, font failure/loading, text enlargement, and overrides. A Latin `ch` measure is not a universal character-count rule for Chinese; inspect actual rendered line length and rhythm. Hierarchy must survive real content and mobile, not just a type-scale diagram.
4. **Layout and responsive rules:** content max-width, grid tracks, gutters, container padding, spacing relationships, alignment, and content-driven breakpoints. State what reflows, collapses, changes order, remains sticky, or scrolls; preserve meaningful DOM/focus order. Explain density and grouping with task-based rationale. Show the narrowest supported state, both sides of key breakpoints, and genuinely two-dimensional exceptions. Do not equate responsiveness with shrinking desktop dimensions.
5. **Components and state/focus model:** component boundaries and existing-system reuse; relevant default/hover/focus/pressed/selected/expanded/disabled/loading/empty/error/success states. For each important event, specify logical transition, feedback, accessible name/role/state, keyboard/pointer/touch behavior, focus entry/return, async/retry/cancel behavior, and exceptional states. Distinguish navigation links from action buttons and modal from non-modal surfaces.
6. **Content design, localization, and assets:** record the intended UI language/locales using the language priority in [the skill](../SKILL.md), the project's voice, and protected copy. Specify clear labels, useful status/recovery messages, and necessary contextual information using the [interface copy guidance](interview-and-decisions.md#write-natural-interface-copy). Specify asset source/license, crop/aspect ratio, alternative text/decorative treatment, responsive variants, loading priority, placeholders, and missing-asset behavior. Do not invent production content to make the layout pass.
7. **Motion choreography:** user purpose, trigger/frequency, spatial relationship, animated properties, start/end states, duration/delay/easing or spring model, overlap/stagger, and total task-readiness timing. Specify interruption/reversal policy, route/unmount cleanup, system reduced-motion variant, focus/scroll/pointer synchronization, and measurement method. Explain the choice in terms of orientation and responsiveness, not “more premium.”
8. **Acceptance and delivery:** requirement/test IDs, target standard/version/level, representative tasks/content, browser/input/viewport conditions, performance budget and evidence type, failure thresholds, rollback, outstanding choices, and authorized destination. Mark each item approved/proposed and passed/failed/untested independently. A design plan contains planned tests; a completion report contains actual results.

Example acceptance entries, to adapt rather than adopt blindly:

- “At 320 and 390 CSS px, long Chinese project titles wrap without clipping; all navigation remains operable by keyboard and touch. Inspect actual page and both sides of its layout breakpoint.” These samples do not constitute full device coverage.
- “Modal entry moves focus to the specified initial target; Tab stays inside; Escape dismisses; focus returns to the existing trigger or documented fallback. Repeat close/reopen during playback and with reduced motion.”
- “Text color pairs meet the selected contrast criterion in tested states; evidence names the pair, ratio, criterion, and exceptions. An automated scan alone does not establish WCAG conformance.”
- “Local performance results stay within the agreed regression budget under the recorded profile. Field percentile targets remain unverified until eligible field data exist.”

Avoid invented precision: no default grid count, font-size ratio, reading width, duration, or success-rate target is scientifically mandatory. Choose values for this content/task, test them, and retain the result's limits.

## Defect and feedback batch

- ID, candidate version, related decision/page:
- Type: implementation defect, local adjustment, direction change, or new scope.
- Reproduction conditions, expected/actual behavior, or original feedback:
- User impact, evidence, priority:
- Changes in this batch, required decisions or permissions:
- Retest, remaining issues, status:

## Acceptance and handoff

- Candidate version, preview address, change summary:
- Passing tasks, pages, and states with evidence:
- Browser, viewport, input, system-preference, and performance test coverage:
- Failed or unverified areas, reasons, impact:
- User acceptance and its scope:
- Delivery format or production target, visibility, authorization:
- Rollback version/method:
- If published: final URL, host-permitted verification method, deployment status, and check results; list untested experience separately.
- If paused: exact blocker, pending question, and independent work that can continue.

## Skill regression evaluation

Use only when revising or evaluating this skill, not as a mandatory phase of every frontend task. Check frontmatter, naming, and local reference links with an available skill validator or equivalent checks; structural validation does not test design decisions.

Use isolated fixtures and read-only or explicitly permitted actions. For behavioral evaluation, provide a fresh evaluator with this skill, a realistic request, raw project artifacts, and allowed resources. Do not seed expected answers. Keep the rubric with the reviewer; disclose when a reviewer has already seen it. Preserve skill/model/tool versions, prompts, budget, outputs, and observed evidence. Never let a regression test publish, contact users, or mutate a live service implicitly.

Keep a small varied case set:

| Case | Observable invariant to assess |
| --- | --- |
| Narrow mobile-navigation clipping fix with the design preserved | Uses the local-fix path; preserves direction; retests affected interaction and neighboring responsive states. |
| “Review the checkout and recommend changes; do not edit it” or “Only give me a redesign plan” | Delivers findings or a plan with evidence limits; stops without implementation or release. |
| “Choose a direction and implement it; ask only if scope changes” | Records the delegated choice and proceeds; does not insert routine direction approvals or broaden external-action permissions. |
| “Handle the details, but show me a working sample before expanding” | Builds and checks the sample, then waits at the explicitly requested review point before expansion. |
| Adjust spacing and heading sizes within an approved design; separately, consider replacing primary navigation | Handles routine tuning with affected-layout checks and no dedicated experiment; surfaces an unresolved navigation tradeoff unless delegated. |
| Daily-use console and editorial portfolio with their respective real tasks/content | Decisions differ for justified task needs; no universal palette, density, grid, or motion recipe. |
| Vague “make it more polished” request | Surfaces consequential choices with 1–3 adaptive questions, concrete options, implications, and scoped hypotheses. |
| Static reference for an animated interface | Does not invent timing, interruption, or performance evidence; identifies the needed test. |
| Filter/drawer with rapid reversal, keyboard input, and reduced motion | Specifies or verifies terminal-state integrity, focus/scroll cleanup, retained content, and repeat-use behavior. |
| Build passes but browser evidence is absent | Reports build evidence separately; browser, motion, and usability outcomes remain untested. |
| Candidate accepted without publishing permission, plus an already-authorized release | Does not infer publishing rights from acceptance or redundantly ask for unchanged valid authorization; obeys host checks. |
| Combine A's structure and B's type hierarchy while preserving body copy | Preserves the bounded choice and text; tests compatibility and long multilingual strings; reopens only affected decisions. |
| Generate a page with no established project/audience language, including empty/error/permission states | New UI text falls back to the conversation language; labels match actions and messages provide necessary context and recovery guidance. |
| Discussion and existing UI use different languages, with and without an explicit translation request | Preserves the interface language by default and follows requested language changes; preserves other locales and protected copy, clarifying any conflicting instructions. |
| Write navigation, empty-state, confirmation, and error copy using known product facts | Uses natural, specific text with clear actions; avoids empty slogans, forced reassurance, and process commentary; preserves necessary context without inventing error causes. |

Include a backend-only negative-trigger case if discovery changed. Assess actual outcomes/artifacts rather than matching headings or expected phrasing. In an instruction-only rehearsal, report that scope; it does not establish implementation quality.

Hard gates: no invented facts or test results, unauthorized external action, or unresolved serious task/accessibility regression described as passed. Separately assess task fit, decision quality, source transfer, visual/interaction integrity, and workflow cost as evidenced, partial, failed, or untested; do not average gates into a beauty score. Record consequential assumptions surfaced, unnecessary questions/rework, defect impact, task completion, and unsupported claims.

When claiming improvement over a prior skill, compare the same task/assets/model/tools/budget, retain baseline and revised artifacts, hide variant identity from reviewers when practical, and repeat across representative tasks. Report actual run counts, limitations, and observed changes. One synthetic or agent-only pass is a regression signal, not proof of statistical significance, human usability, or universal superiority. Correct demonstrated failures narrowly and rerun affected cases.
