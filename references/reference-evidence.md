# Reference Evidence

## Audit the project before collecting inspiration

Verify the target URL, routes, version, and environment. Read existing design agreements. Open the current site. Use source code to explain tokens, states, and component ownership; use screenshots to document a particular viewport at a particular time; use actual interaction to support behavioral conclusions.

Choose representative coverage: an entry page, a major inner page, a key task, and desktop and mobile viewports. Sample complex sites by template and state. Do not describe a sample as full-site coverage. Record login, data, region, and tooling limitations.

Prioritize these questions:

- Is the primary task clear, and does content hierarchy support the goal?
- Which identity cues, structures, and existing interactions deserve preservation?
- How does real content wrap, align, crop, and affect density and reading length?
- What states and paths exist for navigation, menus, forms, filters, and disclosure controls?
- Does mobile retain the necessary desktop functionality, without hiding essential content to “fix” the layout?
- Does motion explain state, or obstruct clicks, reading, and repeated use?

Report a few highest-impact findings. Give the observation, consequence, specific recommendation, and validation method for each. “Not premium enough” is not a reproducible finding.

## Classify evidence before using it

Use these distinctions in project records; labels need not clutter the user conversation:

- **Normative requirement:** name the standard, version, criterion, conformance level, applicability, and exceptions. A criterion being mandatory for a selected conformance target does not by itself establish a legal obligation for this project.
- **Measured observation:** include task/state, version, environment, method, result, and uncertainty. A single observation supports that observation, not a population claim.
- **Design heuristic:** an informed starting point, such as proximity for grouping or stronger size contrast for hierarchy. State the task-based rationale and countervailing costs; test in context.
- **Proposed parameter or hypothesis:** a type scale, grid count, line length, duration, easing curve, or budget chosen for trial. For a consequential trial, state a failure condition and whether it is approved and validated; routine tuning only needs the relevant quality checks.

Do not launder heuristics into scientific laws. An 8-point spacing scale, golden ratio, fixed line length, particular font pairing, or 200 ms animation is not universally optimal. Brand expression and aesthetic preference remain legitimate criteria without pretending they are experimentally proven. Official design-system guidance is authoritative for its own system, not universal evidence of superiority.

For consequential decisions, link requirement → evidence → decision → implementation → test/result. Revisit the affected link when facts or goals change. See [traceability](project-templates.md#requirements-to-tests).

## Research a specific problem

Search for concrete questions such as “mobile navigation for a project index with long titles,” rather than only “best-looking websites.” Start with user-provided references and products serving similar tasks, then seek transferable mechanisms elsewhere. Treat galleries, awards, and aggregators as starting points.

Open relevant pages on the original sites and interact whenever possible. Inspect desktop and mobile, normal states, and important exceptions. For references with unusually strong assets, test whether the mechanism still works with this project's assets. Compare opposing approaches when useful examples are available and explain why each works in its context.

Record for each reference you adopt:

- Original URL, page/state, inspection date, and method.
- Evidence location: screenshot, short recording, interaction log, or source location.
- Observed structure or behavior and the corresponding project problem.
- Transferable principle and elements that should not be copied.
- Asset/code permissions; analyze without reusing assets when rights are unknown.
- Claim status: observed, reported by a source, inferred from implementation, or unverified.

Do not infer precise easing, delay, interruption handling, or performance from static screenshots. Treat an author's claim of “smoothness” as their assessment. Mark motion you have not played as untested and propose a test when needed. Never invent sites, screenshots, browsing results, or designer intent.

## Turn references into design directions

Define comparison axes before producing 2–3 project-specific directions. Make at least one core mechanism meaningfully different: selected narrative versus index browsing, linear reading versus a sectional overview, or direct action versus progressive disclosure. Explain how any difference in visual character serves the goal.

Hold core copy, data, main images, user task, viewport, and comparison scope constant. Do not give one candidate real content and another polished fictional copy, then attribute the difference to design.

Provide for each direction:

1. Project goal and problem addressed.
2. Information order and key layout.
3. Typography, density, color roles, and interaction/motion strategy.
4. Desktop first screen, one important downstream section, and mobile structure.
5. Benefits, sacrifices, risks, and conditions for suitability.
6. Reference mechanisms, your recommendation, and hypotheses to validate.

Name directions to explain their differences. Do not hide identical structures behind abstract slogans. When the user has chosen a direction, explore only unresolved consequential points rather than deviating from the brief to manufacture options.

## Keep prototypes small and comparisons real

Use dedicated comparisons for unresolved tradeoffs, difficult judgments, or costly rework. Routine tuning within the chosen direction needs checks of the affected layout or behavior, without a separate experiment or comparison document.

Use an authorized isolated project location or the existing preview workflow. Do not replace production paths without approval. Build necessary actions with real DOM text and controls. Images may communicate a visual idea but cannot stand in for a working interface.

Start with the riskiest segment: first screen and following section, list and detail, critical form, or mobile menu. Show one version at full size, then switch under the same conditions. If you provide side-by-side screenshots, also provide an operable version.

Write one hypothesis and one failure condition per experiment. For example: “Exposing the main entry lets returning visitors reach the index in one fewer action; the layout fails if real labels overflow on narrow screens.” Do not describe personal preference as user-research evidence.

State causal limits when content, typography, structure, and motion change together. Narrow variables and test again if you cannot tell which change caused an effect. Preserve useful earlier candidates; the latest version is not inherently better.

## Check task success, not only preference

Choose a realistic critical task and define success/failure before the session: for example, find an eligible item, identify its key constraint, then reach the correct detail view. Use neutral prompts that do not name the intended control. Record unaided completion, assistance, errors, recovery, and the participant's explanation; measure time or action counts only when relevant and under comparable conditions. If think-aloud or coaching changes timing, disclose it.

Test with actual or likely users when authorized and available. Follow [GOV.UK's moderated-testing method](https://www.gov.uk/service-manual/user-research/using-moderated-usability-testing). A review by the owner or another agent is valuable but is not representative-user evidence. A small formative sample finds issues; it does not establish a stable conversion lift or population success rate. Report counts with denominators and the recruitment/task limitations. If claiming a causal benefit, use an appropriate controlled study and uncertainty analysis rather than relabeling a preference comparison as an A/B experiment.

Include disabled users when feasible and authorized, without treating their individual results as proof of complete accessibility; see [WAI's evaluation guidance](https://www.w3.org/WAI/test-evaluate/involving-users/). Do not recruit, record, transmit personal data, or install analytics without the required authorization. When users or instrumentation are unavailable, provide a test plan and mark outcomes unverified.

## Stop research when the decision is supported

Move to a decision once there are relevant references, comparable prototypes, and clear tradeoffs. Do not substitute collecting links for progress. Research again when a significant new constraint appears.

A cited article or open-source project establishes what its source proposes, not that the method is necessarily better for this project. Distinguish author demonstrations, personal reports, reproducible experiments, and normative requirements. Test aesthetic advice against project outcomes rather than popularity, downloads, or automated scores.

Before reusing third-party assets or code, verify the exact source, version, license, and usage rights. Learning from a principle does not authorize copying a site, trademark, photograph, or distinctive creative work. See the attribution and reuse guidance in [Sources and evidence limits](sources.md).
