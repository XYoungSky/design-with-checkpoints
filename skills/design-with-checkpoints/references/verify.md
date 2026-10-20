# Verify

Check the changed pages, states, and paths, and widen the check when the change touches shared components or global styles. Use a real browser: the host's browser tool, Playwright, or Puppeteer. If no browser is available, run the checks you can and report rendered behavior as untested.

## Look at screenshots

Capture each changed page and state at 320, 390, 768, 1280, and 1440px wide, plus any widths the audience mainly uses. Open the screenshots and look at them; a file on disk is not a review. Compare them with the chosen direction, then run the [layout check](layout-and-type.md#layout-check).

A screenshot shows one frame. It does not prove that an interaction or animation works.

## Test interaction and motion

- Keyboard: Tab and Shift+Tab order, visible focus, Enter and Space on controls, Escape on overlays, focus returning to the trigger after a dialog closes.
- Touch: everything that appears on hover also works with a tap or focus.
- Motion: every row of the [motion inventory](motion.md#motion-inventory) at normal speed, with rapid repeated input, and with `prefers-reduced-motion: reduce`.
- Paths: primary actions, navigation, links, refresh, and the browser back button. Test forms with safe data; never send real messages or orders without permission.
- Console and network: no errors and no failed requests.

## Accessibility essentials

Use the project's target, or WCAG 2.2 AA when none is set:

- text contrast 4.5:1, large text 3:1; control boundaries and focus indicators 3:1;
- content reflows at 320px width without scrolling in two directions;
- text enlarged to 200% loses no content or function;
- pointer targets at least 24 × 24px, or spaced to the same effect;
- focused elements are never fully hidden by sticky headers or overlays;
- headings, landmarks, labels, and accessible names are present and accurate.

An automated scan such as axe finds only part of these problems. A clean scan is not a pass.

## Content

Check real content in every supported language, the longest strings, and the empty, loading, error, and success states. No placeholder text remains in delivered work unless it is labeled as a placeholder.

## Performance

Measure only when motion, loading, or an agreed budget makes performance part of the task. Record the browser, device or emulation, and network profile with the result. A build passing or a Lighthouse score does not show how a real interaction feels.

## Report honestly

Separate three kinds of claims: what you observed in a browser, what you inferred from the code, and what you did not test. Device emulation is not a physical device. A successful build is not a tested interface.

Handoff:

```text
Changed: what changed, with links to files or a preview.
Decisions: consequential choices and who approved them.
Motion: the chosen intensity and the final motion inventory.
Checked: widths, browsers, keyboard, reduced motion, languages.
Failed or untested: with the reason and the effect on users.
Next: the one thing the user needs to decide or do, if any.
```

Recommend release only when no serious functional, content, layout, or accessibility problem remains. Publishing or deploying needs the user's permission even after the design is approved.
