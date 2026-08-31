# Task 016 — Strict mode

**Concept:** JS's default (non-strict) mode silently allows things that are almost always bugs —
assigning to an undeclared variable creates an accidental global, and `this` inside a plain
function call defaults to the global object instead of `undefined`. Strict mode turns those into
loud errors instead of silent footguns. It's also worth knowing *why* you rarely have to think
about this day-to-day: ES modules and classes are strict by default.

**Where this goes:** concept-lab, and honestly a mostly-background one — since `project/` is built
as ES modules from task 027 onward, you get strict mode automatically and this specific bug class
mostly won't recur there. The real payoff is knowing *why* you don't have to think about it, not a
project task that revisits it.

**Step 1 — build it yourself, no AI:** in a plain (non-module) `.js` script with no `"use strict"`,
write a function that assigns to a variable you never declared with `let`/`const`/`var` (e.g.
`total = 0` instead of `let total = 0`) inside a function, then log it from outside that function
to confirm it leaked into the global scope. Predict what will happen to the exact same code if you
add `"use strict"` at the top of the file — then add it and confirm. Also confirm, without strict
mode, what `this` is inside a plain function called with no receiver (`someFunction()` at the top
level) — then confirm what it becomes with strict mode on.

**Done when (step 1):** you've demonstrated the accidental-global leak actually happening, your
prediction for what strict mode does to it is written down before testing, and you've confirmed
both the non-strict and strict values of `this` in a bare function call.

**Step 2 — AI review pass:** ask: "I write all my real code in ES modules, which are strict by
default — given that, is this task's specific accidental-global bug something I actually need to
guard against day-to-day, or was I just learning what a legacy script would have let through?
Give me one real scenario, if any exists, where I could still hit a non-strict-mode bug in a
modern project." Note the answer in `PROGRESS.md`.

**Stretch (optional):** none — this is a short, focused task.
