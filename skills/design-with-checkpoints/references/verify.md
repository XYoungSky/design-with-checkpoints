# Verify

Keep verification light: take a few screenshots and read the code. The user judges how the page looks and moves on the live page.

## Screenshots

Take only the screenshots you need: each changed page once at 390px and once at 1440px, with a headless browser or the host's screenshot tool. Look at them and run the [layout check](layout-and-type.md#layout-check). Add a screenshot of a particular state, such as an open menu, only when the change is about that state.

Do not use computer use or desktop control, step through the page click by click, capture frame sequences, or record videos. Without a screenshot tool, say that the rendered page is unchecked.

## Read the code

Check the changed code for:

- **Layout:** fixed widths or heights that can overflow at 320px; text under 12px; text colors below 4.5:1 contrast on their background (3:1 for large text).
- **Semantics and keyboard:** real buttons, links, inputs, and labels; a visible `:focus-visible` style; Escape closes overlays; hidden content cannot receive focus.
- **Motion:** every animation appears in the [motion inventory](motion.md#motion-inventory); transitions retarget from the current state; no state waits on `animationend`; a `prefers-reduced-motion` path covers both CSS and JavaScript animation.
- **Content:** real text, no leftover placeholders, and [interface copy](alignment.md#interface-copy) that fits the project.
- **Errors:** obvious script errors, missing files, broken links.

## Only when asked

Browser automation, scripted keyboard runs, text zoom, touch emulation, performance traces, cross-browser runs, and screen-reader checks.

## Report honestly

Say which screenshots you looked at, what you checked in the code, and what you did not test. A successful build is not a tested interface.

Handoff:

```text
Changed: what changed, with a link to the page or files.
Decisions: consequential choices and who approved them.
Motion: the chosen intensity and the final motion inventory.
Checked: screenshots taken and code reviewed.
Untested: what was not checked, if it matters.
Next: the one thing the user needs to decide or do, if any.
```

Publishing or deploying needs the user's permission, even after the design is approved.
