# Layout and Type

The values below are starting points, not standards. Begin with them, adjust after looking at the real content, and give the reason when you depart from them. The type rules cover Chinese and English; rules marked general apply to both.

## Start from the content

Before choosing a layout, list what the page must hold: the longest real heading, the number of items, image aspect ratios, and the one action that matters most. Each screen gets one focal point. The layout serves the primary task first; decoration comes last.

## Composition moves

Use these as the vocabulary for directions. Pick by task, not by habit.

| Move | Use when | Costs |
| --- | --- | --- |
| Editorial column: one reading column, wide margins | Long text, case studies, documentation | Little side-by-side comparison |
| Asymmetric split: a dominant column and a supporting one, about 2:1 | A hero with proof, product with details | Needs real content in both columns |
| Index list: dense rows with metadata | Collections, archives, many items | Weak first impression with few items |
| Modular grid: equal cards | Comparing peers of equal weight | Flattens hierarchy; a poor default |
| Sticky aside: navigation or a summary pinned beside long content | Long pages with sections, settings | Needs about 240px or more; collapses on mobile |
| Full-bleed band: a section that breaks the container | One key moment per page | Loses force when repeated |

## Grid and spacing

- Containers: running text 640–760px wide; page content 1120–1280px; full-bleed only on purpose.
- Side gutters: 16–20px on phones, 24–32px on tablets, 32–64px on desktop.
- Spacing scale (general): 4, 8, 12, 16, 24, 32, 48, 64, 96, 128px. Use only scale values.
- Proximity: space inside a group is clearly smaller than space between groups, about 1:2 or more.
- Section spacing: 64–128px on desktop, 48–80px on phones.
- Breakpoints come from the content: add one where the layout breaks, not at device names.
- Alignment: elements share a small set of edges. A near miss of 1–4px reads as a mistake.

## Type hierarchy

General:

- Use at most 7 font sizes per page, from a scale: ratio 1.2–1.25 for dense product UI, 1.333–1.5 for editorial and marketing pages.
- Body text 16–18px; never below 16px for body text on phones. Anything the user needs to read is at least 12px. Text inside an illustration or a scaled-down preview may be smaller only when it is decorative and hidden from assistive technology.
- Build hierarchy with size and weight together; use at most 3 weights.
- Fluid headings: `clamp()` between a phone size and a desktop size, instead of overriding sizes at every breakpoint.
- `text-wrap: balance` on headings and `text-wrap: pretty` on paragraphs where supported.
- `font-variant-numeric: tabular-nums` for numbers that line up in tables or lists.

| Setting | Chinese | English |
| --- | --- | --- |
| Body line height | 1.7–1.8 | 1.5–1.6 |
| Heading line height | 1.3–1.4 | 1.1–1.25 |
| Letter spacing, body | 0 | 0 |
| Letter spacing, display headings | 0; never negative, because the glyphs touch | −0.01 to −0.03em |
| Letter spacing, small uppercase labels | not applicable | +0.04 to +0.08em |
| Line length | 25–40 characters per line | 45–75 characters per line |
| Emphasis | weight or color; no italics | weight, color, or italics |

Fonts:

- Put the English face first and the Chinese faces after it, so Latin characters use the English design: `"Inter", "PingFang SC", "Hiragino Sans GB", "Noto Sans SC", "Microsoft YaHei", sans-serif`. Replace Inter with the project's face.
- Monospace: `ui-monospace, "SF Mono", "JetBrains Mono", Menlo, Consolas, monospace`. Do not rely on the bare `monospace` keyword; it falls back to Courier on Windows.
- Set `lang` on the root element and on any mixed passage, so browsers choose the correct glyphs and line-breaking rules.
- Chinese web fonts are large. Prefer system Chinese fonts, or subset the face to the characters used.
- Check mixed lines such as "使用 Claude Code 构建": the English part must not look larger or sit on a different baseline. Adjust with `font-size-adjust` or choose a pair with matching x-height.

## Color roles

Name tokens by role, not by hue: `--surface`, `--surface-alt`, `--text`, `--text-muted`, `--border`, `--accent`, `--accent-text`, `--danger`. A token named `--red` that holds teal will mislead the next edit. Use one accent for actions and selection, not for decoration. Check text contrast on every background the text actually sits on, tinted panels included.

## Responsive behavior

A phone layout is a re-ordering by priority, not a shrunk desktop. Keep the chosen direction's character: an editorial page stays editorial on a phone. Touch targets are at least 24 × 24px, and 44 × 44px for primary actions. Content that only appears on hover also needs a tap or focus path.

## Template tells

These make a page look machine-made. Avoid them unless the user asks and the reason is recorded:

- pseudo-technical labels with no meaning, such as "FIG. 01", coordinates, version stamps, or fake window dots;
- decorative dot grids, orbit rings, and gradient blobs behind content;
- three icon cards as the default feature section; everything centered;
- important information in tiny uppercase monospace text;
- negative letter spacing on Chinese text;
- more than 7 font sizes, or one-off sizes per breakpoint;
- hover effects on elements that cannot be clicked;
- placeholder names such as "XXX" or lorem ipsum in a sample shown to the user.

## Layout check

Run this on every changed page and state at 320, 390, 768, 1280, and 1440px wide, with the longest real content. Fix each failure, or record why it is acceptable.

1. **Focus.** The primary task and the focal point are clear on the first screen.
2. **Fit.** No clipping, overlap, or horizontal scrolling. Headings wrap evenly, with no single character or word alone on the last line.
3. **Type.** At most 7 sizes; readable text 12px or larger; body text 16px or larger; line height, line length, and letter spacing within the table above.
4. **Spacing.** Only scale values; space inside groups smaller than space between groups.
5. **Alignment.** Elements share edges; no near misses.
6. **Contrast.** Text at least 4.5:1, large text at least 3:1, on its actual background. Control borders and focus indicators at least 3:1.
7. **Mobile.** The priority order and the direction's character survive at 320 and 390px.
8. **Affordance.** Every hover effect, pointer cursor, and underline belongs to something interactive.
9. **Language.** Both Chinese and English versions pass, when the page has both.
