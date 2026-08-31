# Task 003 — Event listeners

**Concept:** `addEventListener` attaches a callback (task 016's concept) to a DOM event — this is
how a static page becomes interactive, and the event object it hands you carries useful data
(`event.target`, `event.key`, etc.).

**Step 1 — build it yourself, no AI:** wire up: a button click that increments a counter shown on
the page, a keydown listener on an input that logs which key was pressed, and a listener that
reads `event.target` to identify which of several buttons (from a loop) was clicked.

**Done when (step 1):** all three listeners work, and you can explain what `event.target` is and
why it matters when the same handler is attached to multiple elements.

**Step 2 — AI review pass:** ask the AI to explain the difference between `event.target` and
`event.currentTarget`.

**Stretch (optional):** add a `removeEventListener` that disables the counter button after 5
clicks.
