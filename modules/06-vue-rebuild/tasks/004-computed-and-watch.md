# Task 004 — Computed and watch

**Concept:** `computed` derives a value that auto-updates when its dependencies change (your
capstone's live total price is a perfect fit); `watch` runs a side effect in response to a change
— knowing which one fits which job is a real design decision, not just syntax.

**Step 1 — build it yourself, no AI:** implement your capstone's live total price as a
`computed` property based on selected rules, and add a `watch` that logs whenever the total
crosses a threshold (e.g. above $1000).

**Done when (step 1):** the total updates automatically as selections change, and the watch fires
only when the threshold is actually crossed (not on every change).

**Step 2 — AI review pass:** ask the AI why using `watch` to derive the total (instead of
`computed`) would be worse practice here.

**Stretch (optional):** add a `computed` with a getter and setter.
