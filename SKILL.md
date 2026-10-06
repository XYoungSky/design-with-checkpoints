---
name: design-with-checkpoints
description: "Design, redesign, and review websites and frontend interfaces using adaptive user checkpoints, evidence-based decisions, interactive prototypes, and real-browser tests. Use for frontend plans, information architecture, layout, typography, interaction, motion, or visual polish. Scale down for local fixes; exclude backend-only work."
---

# Design with Checkpoints

Turn the user's goals into comparable, usable, verifiable designs. Own research, recommendations, and implementation; involve the user in unresolved consequential choices and honor decisions they delegate. Avoid both exhaustive questionnaires and a full-site redesign based only on “make it look better.”

Explain design choices in the user's language, using concrete tradeoffs and defining unfamiliar terms when needed. Follow project conventions for records and preserve code/API identifiers.

For newly authored page and UI content, follow this language priority: explicit user instructions → established project language and confirmed audience requirements → conversation language when neither establishes a choice. Preserve existing locales and protected copy; clarify material conflicts before translating content. Match the project's voice and the audience's vocabulary. Make labels, instructions, and status messages clear and actionable, with necessary context at the point of use. Avoid generic promotional slogans, forced intimacy or poetic reassurance, padded politeness, and commentary about the implementation process. Use concrete actions and facts rather than vague promises. Apply the [interface copy guidance](references/interview-and-decisions.md#write-natural-interface-copy) and include copy in QA.

## Route the task

1. Read the conversation, project conventions, and approved versions. Confirm the target site, scope, and specified environment. Verify discoverable facts yourself; ask only when the target remains ambiguous. Do not guess a repository or reuse another project's assumptions.
2. Take the shortest relevant path: start new work with goals and content; audit before redesigning; inspect only affected paths for local fixes; resume an approved direction at its current stage. Match the requested deliverable: a plan ends with actionable recommendations and proposed checks; a review ends with evidenced findings and priorities. Continue into implementation only when requested. Do not repeat answered questions to satisfy a process.
3. Establish the preview and delivery mode: local/file delivery, external preview, or production update. Record the target, visibility, existing authorization, and change batches. Follow the host's site-building, hosting, upload, and publishing policies first. This skill neither expands permission nor overrides those policies. Continue permitted local work while required authorization is pending.
4. Load only references needed for the current stage:
   - Read [Interview and decisions](references/interview-and-decisions.md) when asking questions, choosing directions, or resolving feedback.
   - Read [Reference evidence](references/reference-evidence.md) when auditing sites, researching references, or comparing prototypes.
   - Read [Motion and QA](references/motion-and-qa.md) when designing motion, testing in a browser, or preparing acceptance.
   - Use [Project templates](references/project-templates.md) when preserving context or preparing a handoff.
   - Read [Sources and evidence limits](references/sources.md) when checking attribution, evidence strength, or third-party reuse.

For a local fix: reproduce → identify the affected layout/state/token → make the smallest authorized change → retest the affected path and nearby regressions → report evidence. Skip direction variants, broad interviews, and full-site specifications unless the fix exposes a consequential choice.

## Apply these rules throughout

- Put user goals, real content, and established brand facts before aesthetic advice. Do not excuse functional, accessibility, or factual failures as style.
- Do not turn one project's palette, fonts, cards, radii, density, or motion intensity into defaults for every site. Do not replace one formula with another.
- Judge designs using real content. Label temporary data and assets. Never invent clients, results, quotations, testimonials, or business commitments.
- Usually ask only 1–3 questions that change the next step. Give project-specific evidence, a concrete recommendation, viable alternatives, and their costs. Resolve dependencies first; do not ask the user to supply facts you can verify.
- Distinguish recommendations, experimental values, and approved decisions. Silence is not approval. Liking a reference image does not approve a full redesign or public access.
- Use checkpoints for unresolved choices that materially change the user's goal, direction, core interaction, scope, or cost of rework. Existing decisions and explicit delegation satisfy the relevant checkpoint; record the rationale and proceed within that scope. Preserve any review points the user specifically requested.
- Pause work that depends on an unanswered, non-delegated consequential decision. Continue independent audits, research, and low-cost experiments without quietly committing to an unchosen direction.
- Handle pixel-level corrections, missing states, and implementation details within approved scope. For example, replacing primary navigation or changing the checkout sequence warrants a checkpoint when not delegated; tuning spacing, type sizes, or transition timing within an agreed direction normally does not. Reopen only affected decisions when direction, information architecture, core interaction, or scope changes.
- Separate observed behavior, source-code inference, and unverified claims. A screenshot does not prove motion quality, a successful build does not prove usability, and mobile emulation does not prove physical-device behavior.
- Distinguish normative requirements, measured observations, design heuristics, and proposed testable parameters. Record the applicable standard/version/level and exceptions. Neither popularity nor a design system proves that an aesthetic choice improves outcomes.
- Connect each consequential requirement to a design decision, implementation location, and acceptance test. Use a short linked record, not paperwork for every CSS value. Define success before seeing results; report a failed or untested criterion without quietly lowering it.

## 1. Audit and define

Inspect an existing site in a real browser. State whether it is the assistant's browser or the user's browser. Cover the homepage, representative inner pages, key paths, and desktop and mobile viewports. Open menus, switch states, scroll, and navigate. Record the version, URL, viewport, time, and evidence. Use source code to confirm implementation ownership and constraints, not as a substitute for rendered inspection.

Report a few high-value findings: features to preserve, problems with the greatest impact on user tasks, specific changes, and risks. If browser access is unavailable, continue source inspection and permitted local checks, mark rendered and interactive behavior unverified, and identify what remains to test. Do not claim a completed site or motion audit.

Summarize the audience, main task, content priorities, preserved elements, scope, constraints, and acceptance criteria in a short brief. Capture the baseline when comparison matters. Specify the accessibility target, supported inputs/viewports, and evidence needed for task success and performance. Treat unmeasured targets as proposals. Ask only about unsettled goals; do not reconfirm established decisions.

Checkpoint, when goals or scope remain unsettled: resolve what affects information architecture before choosing the overall structure and visual direction. Research references in parallel while dependent implementation waits.

## 2. Research and propose directions

Find real sites serving related user tasks, then add typography, navigation, or interaction examples. Explain the problem each reference solves, the mechanism worth adapting, and what cannot transfer. Do not deliver only inspiration links or rely on rankings.

For substantial exploration, propose 2–3 meaningfully different directions. Use the same confirmed content and show a desktop first screen, one important downstream section, and the mobile structure for each. Differentiate information order, layout, density, visual language, or interaction model. Three palettes are not three directions.

Explain each direction's project fit, main benefits, real sacrifices, and untested risks. Recommend one and give the evidence. Do not manufacture alternatives when the user has already specified a direction or restart full-site concepts for a narrow change.

Checkpoint, when direction is neither chosen nor delegated: obtain the main direction and important layout choices. If the user wants a combination, preserve the specified parts and resolve consequential conflicts. Record the decision before proceeding.

## 3. Choose through small interactive prototypes

Build the smallest complete segment that can test the direction, such as the first screen and following section, browsing to a detail view, or mobile navigation. Keep content and comparison conditions consistent. Show each candidate at normal size and make it operable; reduced screenshots cannot replace use.

Use paired samples when an unresolved typography, layout, or motion choice has a meaningful tradeoff, is difficult to judge directly, or could cause substantial rework. For routine tuning within the chosen direction, implement and check the affected result directly. For an actual experiment, state the hypothesis, controlled conditions, and failure criterion before testing. A prototype may test compatible hypotheses together, but do not change every variable and claim to isolate its effect. Distinguish user preference, expert inspection, and observed task completion. Do not build three complete sites unnecessarily.

Define the purpose, trigger, states, repeat frequency, interruption/reversal behavior, touch and keyboard behavior, reduced-motion alternative, and measurement method for important animations. Demonstrate normal-speed and repeated use. Edited recordings and the presence of code do not establish a passing test.

Checkpoint, for unresolved choices or a requested sample review: show the working sample and wait for that decision before expanding sitewide. When no such checkpoint remains, verify the sample and continue within the approved or delegated direction. Approval of a sample does not establish acceptance of unseen pages or exceptional states.

## 4. Implement within approved scope

Capture the direction as an implementable frontend specification using [Project templates](references/project-templates.md#frontend-specification). Include semantic design tokens, type hierarchy, grid and responsive rules, component/state and focus models, assets, motion choreography, and measurable acceptance criteria. Specify values, units, behavior, rationale, and approval/test status where they affect implementation. Reuse existing records; do not invent a new token system unnecessarily.

Complete one working vertical slice with real content, desktop and mobile behavior, necessary exceptional states, and reduced-motion support. Then extract shared components and expand to remaining pages. Respect the existing stack and component system. Do not automatically add frameworks, animation libraries, hooks, or installers to use this skill.

Work in batches organized around verifiable user paths. Fix implementation that diverges from approved decisions. Request a new decision only for a new constraint, consequential tradeoff, or scope change. Preserve valuable earlier candidates; do not add complexity indefinitely to improve a self-assigned score.

## 5. Inspect, retest, and seek acceptance

Inspect the running page for hierarchy, typography, proportion, cropping, content rhythm, and cross-page consistency. Also test core paths, keyboard and touch use, responsive behavior, loading/error states, console output, and performance. Use [Motion and QA](references/motion-and-qa.md) to test repeated input, interruption, reversal, and system reduced-motion preferences.

For substantial or uncertain changes, use an independent reviewer when available and permitted, with the brief, approved direction, and version, without seeding conclusions. For user testing, use neutral task prompts and record unaided success, assistance, errors, and recovery. An agent walkthrough is not human usability research. Automated scans and model scores cannot replace visual judgment and real interaction.

Retest fixes under the original reproduction conditions. Report tested scope, untested scope, and remaining impact. Do not recommend release with unresolved serious functional, content, responsive, or accessibility problems. When user acceptance is a requested or agreed checkpoint, present an identified candidate version and wait for that decision rather than asking an abstract “Are you happy?” Otherwise, deliver the verified result within existing authorization without adding a confirmation step; distinguish completed checks from user acceptance.

## 6. Consolidate feedback and deliver as authorized

Classify feedback as an implementation defect, local adjustment, direction change, or new scope. Consolidate related changes into one candidate preview and review the batch. Do not automatically turn every small comment into a production deployment. Reopen only affected decisions and tests.

Record design approval, candidate acceptance, and publishing authorization separately. Do not mechanically reconfirm valid authorization when the target, version scope, and risk remain materially unchanged. External uploads and publicly accessible previews must also comply with current policies and permissions. Handle an urgent production fix according to its actual authorization and risk; do not bundle in an unapproved redesign.

Deliver the requested plan, review, or identified implementation in the user's language. For implementation, summarize consequential design decisions, changed behavior, acceptance results, and pending tests; link the specification rather than repeating it. Include the access method and unverified scope. For an authorized release, verify the target and rollback method, complete necessary preview QA, and perform production checks permitted by the current host. Report deployment status and experience verification separately.

Stop when the requested plan/review or agreed files/preview are delivered, or the authorized release passes the agreed production checks. A necessary decision or permission blocker may also stop dependent work. Do not polish indefinitely, expand scope without approval, or infer verified production behavior from deployment-process success.
