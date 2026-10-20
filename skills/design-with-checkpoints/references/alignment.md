# Alignment

## Restate the brief

Before asking anything, show the user what you understood. Keep it short enough to correct at a glance:

```text
Audience: prospective clients looking for a product designer
Primary task: judge the work quickly, then get in touch
Content: 3 projects with images, a short bio, an email address
Constraints: static site, Chinese and English
Success: a visitor reaches a project in one click and finds the contact link
Open decisions: homepage order, project page density, motion intensity
```

Mark anything you inferred rather than read as inferred.

## Choose questions that change the design

Ask in dependency order, because later answers depend on earlier ones: goal and audience → content priority → structure and layout → type and visual character → motion → acceptance. Skip anything the brief, the code, or the content already answers.

A question is worth asking only when:

- it names a specific page, element, content item, or state;
- it resolves one open decision;
- its possible answers lead to visibly different designs.

Drop broad prompts such as "What style do you like?" or "What should we improve?". Drop questions whose answers would leave the next step unchanged. Never pad a round to reach a number.

## Phrase each question

Pattern: **decision and evidence → 2–3 options with visible effects → recommendation → custom answer.**

> The homepage has 12 projects, and three show the main service best. What should a first-time visitor see first?
> A. **Selected work** — the three projects large, full index one click away. Clear story; unfeatured work takes an extra step.
> B. **Full index** — all 12 as a filterable list. Fast for targeted browsing; weaker first impression.
> C. **Selected, then index** — both on one page. Serves both visitors; a longer page.
> I recommend A: your clients hire you for the main service. Or describe your own order.

Rules:

- Options must all be viable and differ in outcome, not in wording. Avoid loaded pairs such as "premium / basic".
- Keep a genuinely binary choice at two options. Facts such as a URL or a brand color take direct input.
- Explain technical terms by their effect: "a sticky header stays visible while scrolling, which costs about 64px of screen height."
- Ask about the experience, not parameters. Choose durations, curves, and pixel values yourself after the checkpoint.

## Use native question tools

Use the host's structured question tool when it exists, such as AskUserQuestion in Claude Code or the equivalent in Codex. Follow its schema and per-call limits, put the recommended option first, and split a round across calls when the limit is lower than the round. Without a suitable tool, write the questions as numbered text. A preselected option is not an answer; wait for the user.

## Turn taste words and references into decisions

Words such as "modern", "clean", "premium", or "高级感" do not settle a design. Translate them into concrete axes and ask about the axis that is actually open:

| Axis | One end | Other end |
| --- | --- | --- |
| Density | Generous space, one idea per screen | Compact, many items visible |
| Type contrast | Large display headings | Even, quiet hierarchy |
| Composition | Asymmetric, editorial | Regular grid |
| Color | Restrained neutrals, one accent | Saturated, multiple colors |
| Motion | Instant changes | Expressive transitions |

When the user shares a reference site, ask which part they like (structure, typography, color, or motion) and show how that part would look with their content. Learn the mechanism; do not copy assets, branding, or code. Liking a reference approves that part only.

## Present directions

A direction is a design idea plus the moves that realize it. Name it by its difference:

```text
B. Index-first archive
Idea: the work is the hero; the page reads like a catalogue.
Layout: full-width list, one row per project with year, type, and a small image;
        hover or focus expands the row.
Type: one size step between titles and metadata; tabular numerals for years.
Motion: row expansion 200ms ease-out; no page-load animation.
Gains: fast scanning, honest about volume.
Costs: weaker emotional first impression; needs at least 8 projects to feel full.
```

Show each direction as a sample with the same real content, so the user compares designs and not content. List its animations as draft rows of the [motion inventory](motion.md#motion-inventory), so the user sees what will move before anything is built. Recommend one.

## Record decisions

Keep one line per consequential decision in the project's existing notes or in the handoff:

```text
D3 Homepage order: selected work first. Reason: main service. Approved by user, 2026-10-20. Replaces D1.
```

Statuses: pending, approved, superseded. Keep the reason when a decision is replaced, so discarded directions do not come back unnoticed. An unanswered question stays pending; a timeout is not consent. Approval of a design is separate from permission to publish.

## Interface copy

New interface text follows, in order: the user's explicit instruction, the project's established language and voice, the conversation language. Preserve existing locales and protected copy such as legal text.

When the voice is unsettled, show three short versions of one real heading or button and let the user pick. After that, apply the chosen voice to every label and state.

Write text that names the action, object, or state. State errors from known facts and give a next step; do not invent a cause. Keep process notes and design commentary out of the interface.

| Context | Avoid | Prefer |
| --- | --- | --- |
| Project navigation | "开启灵感之旅，探索无限可能" | "查看项目" |
| Empty saved list | "这里静候着与你的美好相遇" | "还没有收藏" |
| Save confirmation | "We're delighted to let you know your changes have been saved!" | "Changes saved." |
| Upload failed, cause unknown | "Oops! A little hiccup interrupted your journey." | "Upload failed. Try again." |
