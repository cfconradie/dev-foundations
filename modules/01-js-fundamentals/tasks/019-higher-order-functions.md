# Task 019 — Higher-order functions

**Concept:** a function that takes or returns another function — this is the pattern behind
`.map`/`.filter` (task 007), event handlers (module 02), and middleware (module 04), so building
your own makes all of those click as one idea instead of separate tricks.

**Where this goes:** concept-lab — `myMap`/`myFilter` themselves aren't reused, but understanding
what `.map`/`.filter`/`makeDiscount` (task 018) actually are under the hood is what makes task
028's real pricing code something you can debug, not just something that happens to work.

**Step 1 — build it yourself, no AI:** write your own `myMap(array, fn)` and `myFilter(array,
fn)` from scratch using a plain loop (don't call the real `.map`/`.filter` inside them), then
verify they produce identical output to the built-ins on the same input.

**Done when (step 1):** `myMap`/`myFilter` match `.map`/`.filter` exactly on at least 3 test
arrays.

**Step 2 — AI review pass:** ask the AI to point out any edge case (empty array, array with
`undefined` holes) your implementation handles differently from the real one.

**Stretch (optional):** write `myReduce(array, fn, initialValue)` the same way.
