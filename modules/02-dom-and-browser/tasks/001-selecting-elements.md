# Task 001 — Selecting elements

**Concept:** `document.querySelector`/`querySelectorAll` use the same CSS selectors you already
know from Tailwind/module 00, plus `getElementById`/`getElementsByClassName` — this is how JS
finds the HTML it's going to change.

**Step 1 — build it yourself, no AI:** in a static HTML page with a handful of elements
(headings, a list, buttons with classes), write JS that selects: one element by id, all elements
of a class, and one element by a complex CSS selector (e.g. `ul > li:nth-child(2)`), logging each
to the console.

**Done when (step 1):** each selector returns exactly the element(s) you expected, and you can
explain the difference between what `querySelector` and `querySelectorAll` return (single element
vs NodeList).

**Step 2 — AI review pass:** ask the AI when `getElementById` is still worth using over
`querySelector` (hint: performance in hot loops).

**Stretch (optional):** loop over a `querySelectorAll` NodeList using `.forEach` and confirm it
isn't a real array (try an array method that doesn't exist on it).
