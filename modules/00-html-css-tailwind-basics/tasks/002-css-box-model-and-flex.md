# Task 002 — CSS box model and flexbox

**Concept:** every element is a box (content, padding, border, margin) and flexbox is how you
arrange boxes in a row/column without magic numbers — understanding this is what makes Tailwind's
`p-4`, `flex`, `gap-2` classes make sense instead of feeling like memorized incantations.

**Step 1 — build it yourself, no AI:** using plain CSS (a `<style>` block, no Tailwind yet), build
a 3-card row: cards side by side, equal width, gapped evenly, with visible padding and a border.

**Done when (step 1):** you can explain, for one card, exactly which part of it is padding, which
is border, which is margin, and how `display: flex` on the parent produced the row layout.

**Step 2 — AI review pass:** ask the AI to explain any flexbox property you guessed at rather than
understood (e.g. `justify-content` vs `align-items`) and log the one that clicked.

**Stretch (optional):** make the row wrap to a column on narrow screens using only a media query.
