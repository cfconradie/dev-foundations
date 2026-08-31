# Task 002 — Creating and modifying elements

**Concept:** `createElement`, `appendChild`, `.textContent`/`.innerHTML`, and `classList` are how
JS builds and changes HTML at runtime — the mechanism behind every dynamic UI you've ever used.

**Step 1 — build it yourself, no AI:** write JS that creates 5 `<li>` elements from a plain array
of strings and appends them to an existing `<ul>`, then write a function that toggles a
`highlight` Tailwind class on an element when called.

**Done when (step 1):** the list renders from data (not hardcoded HTML), and the toggle function
visibly adds/removes the class on repeated calls.

**Step 2 — AI review pass:** ask the AI why `.textContent` is safer than `.innerHTML` when
inserting user-provided data, and what attack it prevents.

**Stretch (optional):** remove an element from the DOM with `.remove()` after a delay.
