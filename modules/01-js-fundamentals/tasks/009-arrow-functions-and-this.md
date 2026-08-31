# Task 009 — Arrow functions and `this`

**Concept:** arrow functions don't have their own `this` — they inherit it from where they're
defined — which is exactly why they behave differently from regular functions inside objects and
callbacks, and is one of the most common real-world JS bugs.

**Step 1 — build it yourself, no AI:** build an object with a `counter` value and two methods
that increment it after a `setTimeout`: one written as a regular function, one as an arrow
function. Predict what `this` refers to in each *before* running, then run and compare.

**Done when (step 1):** you can explain in your own words why the regular-function version's
`this` is broken inside the `setTimeout` callback and the arrow version's isn't.

**Step 2 — AI review pass:** ask the AI for the "old" pre-arrow-function fix for this exact
problem (`const self = this` or `.bind`) so you understand what arrow functions replaced.

**Stretch (optional):** trigger the same bug using a regular method called as a plain callback
(`array.forEach(obj.method)`) to see it happen in another shape.
