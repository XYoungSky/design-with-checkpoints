# Motion

The values below are starting points. Adjust them from the user's feedback on the live page, and give the reason when you depart from them.

## Give every animation a job

| Job | What it does | Example |
| --- | --- | --- |
| Feedback | Confirms that input was received | A toggle slides; a selected card gains its border |
| Orientation | Shows where something came from or went | A drawer slides from its edge; a card expands into a detail view |
| Attention | Points to a change the user might miss | A new row highlights briefly |
| Narrative and character | Tells a short story or expresses the brand at a rare moment | A hero sequence that demonstrates the product |

If none applies, change the state instantly.

## Derive motion from the content

Generic entrances look machine-made. Start from the page's story: name the one to three things the product or content does, and give each a movement that shows it.

Example from a page about a design workflow: scattered requirement cards snap into a grid (align); the same content reflows into two layouts (choose); the chosen layout extends into a phone frame (review). The motion explains the product instead of decorating the page.

Motion tells, which make a page feel machine-made:

- every block fading up from below as it enters;
- overshoot or bounce on interface elements;
- the same entrance repeated on every section;
- floating or bobbing decoration;
- a cursor tilt applied to everything.

## Choose an intensity

Intensity is a design choice of its own. Ask it separately from the visual direction: a quiet typographic style does not imply quiet motion.

| Level | Feel | Adds | Default for |
| --- | --- | --- | --- |
| Calm | Quiet and immediate | Feedback and orientation only | Dashboards, tools, forms, documentation |
| Lively | Polished and alive | A hero sequence that shows what the product does, content-driven transitions between states, scroll-linked progress where it explains structure, crisp micro-interactions | Marketing pages, portfolios, launches, promotional pages |
| Expressive | A showpiece | Scroll-linked storytelling, page transitions, pointer-reactive depth and 3D on illustrations | Campaigns, brand sites, demos |

Marketing and promotional pages start at Lively; use Calm only when the user chooses it. At every level, high-frequency interactions keep the frequency budget below.

## Let frequency set the budget

| Frequency | Examples | Budget |
| --- | --- | --- |
| High: many times per session | Hover, tabs, toggles, typing, filters | 150ms or less, or none |
| Medium | Menus, popovers, accordions, dialogs, demo steps | 150–500ms |
| Low: once per visit or less | First view, page transitions, onboarding | Up to 1.2s; an interactive demonstration may run about 4s if its text is readable throughout and the user can jump to any step |

## Make it rich, keep it reasonable

- One focal moment per screen. Everything else supports it or stays still.
- Primary content is readable within 400ms of first paint.
- A sequence plays once, or is tied to the scroll position. It never replays on a timer.
- Interface elements settle without overshoot. Bounce belongs only to playful brands that asked for it.
- Text and controls stay put; illustrations and demonstrations carry the movement.
- Input works at every moment of every animation.

## Techniques

- **Same elements, new layout:** move the actual elements into their next arrangement (FLIP, or the View Transitions API where supported) instead of fading one block out and another in.
- **Drawn lines:** reveal paths, rules, and connectors with SVG `stroke-dashoffset` or `scaleX`.
- **Mask reveal:** `clip-path: inset(0 0 100% 0)` to `inset(0)` for a headline line. Use it once per page, not on every heading.
- **Scroll-driven progress:** CSS `animation-timeline: view()` for progress indicators and structural reveals. Native scrolling stays intact; unsupported browsers show the final state.
- **Spring without overshoot:** use the project's library with critical damping, or this CSS curve: `linear(0, 0.203 8.3%, 0.496 16.7%, 0.713 25%, 0.845 33.3%, 0.92 41.7%, 0.96 50%, 0.98 58.3%, 0.99 66.7%, 0.995 75%, 0.998 83.3%, 1)`.
- **Depth:** layered parallax or a pointer tilt of 8° or less on illustrations, only on devices with a fine pointer.

## Starting values

| Interaction | Duration | Easing |
| --- | --- | --- |
| Hover and press feedback | 100–150ms | ease-out |
| Tooltip, dropdown | 120–220ms in, 100–150ms out | ease-out in, ease-in out |
| Accordion | 180–250ms | ease-in-out on height |
| Drawer, dialog | 220–320ms in, about two-thirds of that out | ease-out in, ease-in out |
| Layout change, same elements | 300–500ms | spring without overshoot, or ease-in-out |
| Drawn line | 300–800ms | ease-out |
| Hero sequence | 0.6–1.2s; a skippable demonstration up to about 4s | ease-out and spring without overshoot |

Curves: ease-out `cubic-bezier(0.22, 1, 0.36, 1)` for entering and responding; ease-in `cubic-bezier(0.55, 0, 1, 0.45)` for leaving; ease-in-out `cubic-bezier(0.65, 0, 0.35, 1)` for moving. Use linear only for opacity loops, progress bars, and spinners. Exits are faster than entrances.

## Off by default

Use these only when the user asks explicitly, and record the purpose in the inventory:

- scroll hijacking: intercepting wheel or touch input to control scrolling;
- any of the motion tells above;
- looping motion next to text people are reading;
- parallax on text, or letter-by-letter reveals of body text;
- content that stays hidden unless a script runs.

## Implementation

- Animate `transform`, `opacity`, `clip-path`, and stroke properties. Use CSS transitions for state changes; for sequences, use the Web Animations API or the project's library and retarget from the current state on reversal.
- Write entrance keyframes with only a `from` state, so each element lands on its own resting style at every breakpoint.
- Cancel animations and timers on unmount, route change, and resize. Never depend on `animationend` to reach a valid state, and make hidden or exiting content `inert`.

## Reduced motion

Under `prefers-reduced-motion: reduce`, show the final state, or use a fade of 150ms or less. Keep every piece of content, state, and control, across CSS, JavaScript, scroll-driven effects, and video. Content that moves for more than 5 seconds also needs a pause control.

## Motion inventory

List every animation in the delivered work, with the chosen intensity at the top. The user sees it three times: as a draft for each direction at checkpoint 2, in full at the sample review, and in its final form in the delivery report. Write it in the user's language with plain column names; for a Chinese-speaking user: 元素 · 触发 · 用途 · 频率 · 时长与曲线 · 中途打断 · 减弱动效时.

| Element | Trigger | Job | Frequency | Duration and easing | Interruption | Reduced motion |
| --- | --- | --- | --- | --- | --- | --- |
| Requirement cards | First view | Narrative: cards snap into a grid | Low | 620ms, spring without overshoot | User can jump to any step | Final layout |
| Filter drawer | Tap "Filter" | Orientation | Medium | 260ms ease-out in, 180ms ease-in out | Reverses from current position | Instant |
| Save button | Press | Feedback | High | 120ms color change | Not needed | Same |

Rules:

- No job means the animation is removed.
- High frequency with a duration over 150ms needs a written reason, or a shorter duration.
- Check by script that every row ends in the right state, also after rapid repeated input and with reduced motion on. The user judges how it feels on the live page.

## Asking about motion

Ask about intensity separately from the visual direction, recommend a level for the product type, and give the user a page to open for each option. Do not ask the user to choose durations or curves.

When the user criticizes a specific animation, replace it with one that fits the content better at the same intensity. Remove or tone down motion only when the user says so; if it is unclear which they want, ask.
