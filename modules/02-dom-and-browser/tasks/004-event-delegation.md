# Task 004 — Event delegation

**Concept:** instead of attaching a listener to every child element, attach one to a shared
parent and use `event.target` to figure out which child was actually clicked — critical once
elements are added dynamically (task 002) after the page loads.

**Step 1 — build it yourself, no AI:** build a `<ul>` where clicking any `<li>` toggles a
"completed" style on it, using a single listener on the `<ul>` (not one per `<li>`), then
dynamically add 3 new `<li>` items and confirm they're clickable too without adding new listeners.

**Done when (step 1):** newly-added list items work immediately with zero extra listener code —
this is the point.

**Step 2 — AI review pass:** ask the AI for a real-world example (outside a todo list) where
delegation is necessary, not just nice-to-have.

**Stretch (optional):** use `event.target.closest()` to correctly handle a click on a nested icon
inside the `<li>`.
