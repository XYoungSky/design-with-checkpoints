# Verify

Keep the review basic and quick. The user judges how the page looks and moves; you confirm that nothing is broken.

## Basic review

For each changed page:

1. **Screenshots** at 390 and 1440px wide. Add 320 when the layout is tight, or the widths the audience mainly uses. Look at them and run the [layout check](layout-and-type.md#layout-check).
2. **One small script**, when a browser tool is available: horizontal overflow, console errors, failed requests, text under 12px, and text contrast below 4.5:1 (3:1 for large text).
3. **Keyboard:** Tab through the main controls once. Focus is visible and never trapped; Escape closes overlays.
4. **Reduced motion:** turn it on once. All content is visible and every control works.
5. **Motion:** confirm by script that animations end in the right state, including after rapid repeated clicks. Do not record videos or frame sequences. Give the user a page to open instead, with the [motion inventory](motion.md#motion-inventory).

Without a browser, run what you can and say that the rendered page is untested.

## Only when asked, or when the change is about it

A five-width matrix, 200% text zoom, touch emulation, CPU throttling, performance traces, cross-browser runs, and screen-reader checks.

## Keep it light

Save only the screenshots you show the user. Keep scratch scripts outside the deliverable and delete them when done. Test forms with safe data; never send real messages or orders.

## Report honestly

Say what you saw in the browser, what you inferred from the code, and what you did not test. A successful build is not a tested interface.

Handoff:

```text
Changed: what changed, with a link to the page or files.
Decisions: consequential choices and who approved them.
Motion: the chosen intensity and the final motion inventory.
Checked: widths, keyboard, reduced motion.
Untested: what was not checked, if it matters.
Next: the one thing the user needs to decide or do, if any.
```

Publishing or deploying needs the user's permission, even after the design is approved.
