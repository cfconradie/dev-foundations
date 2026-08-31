# Task 013 — `call`, `apply`, `bind`, and the `this`-binding rules

**Concept:** task 012 showed you one specific `this` bug (arrow vs. regular function in a
callback) and its one specific fix. This task is the general rule those specifics were instances
of: `this` in a regular function is decided by *how it's called*, not where it's defined, and
there are exactly four ways to decide it — default, implicit (called as `obj.method()`), explicit
(`call`/`apply`/`bind`), and `new`. Knowing the rule means you can predict `this` for code you've
never seen instead of memorizing individual gotchas.

**Where this goes:** concept-lab, but the fourth binding rule (`new`) is the direct setup for
tasks 014–015 — prototypes and classes are literally built on that rule, so this is required
groundwork, not a detour.

**Step 1 — build it yourself, no AI:** write one plain function `describe()` that logs `this.name`.
Before running anything, predict what `this` will be in each of these four calls, then run them
and check: (1) calling `describe()` on its own; (2) calling it as `someObject.describe = describe;
someObject.describe()`; (3) calling `describe.call({name: "explicit"})`; (4) calling it with `new`
(you'll need a small tweak so it doesn't error — a constructor-style function that sets
`this.name`). Then write `bind` into the mix: take your task-012 regular-function counter method,
fix its broken `this` using `.bind(this)` instead of switching to an arrow function, and confirm
it now works identically to the arrow-function version.

**Done when (step 1):** your four predictions are written down before running, all four actually
ran and you know which predictions were right or wrong, and the `.bind()` fix for task 012's bug
works.

**Step 2 — AI review pass:** paste your four predictions and actual results, and ask: "For any
prediction I got wrong, explain specifically which of the four binding rules I misapplied and why
— then give me one line of code, different from all four examples I already tried, where it's
genuinely ambiguous which rule applies without knowing how it's called." Note the answer in
`PROGRESS.md`.

**Stretch (optional):** use `.apply()` instead of `.call()` for the explicit-binding example and
explain the one difference between them.
