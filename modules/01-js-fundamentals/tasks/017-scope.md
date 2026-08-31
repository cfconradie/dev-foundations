# Task 017 — Scope

**Concept:** scope is *where a variable is visible* — global, function, and block scope, plus
`let`/`const` block-scoping vs `var`'s function-scoping — is the mental model that makes closures
(next task) make sense instead of feeling like magic.

**Step 1 — build it yourself, no AI:** write a small script that deliberately demonstrates: a
variable shadowed inside a block, a `var` "leaking" out of an `if` block where a `let` wouldn't,
and a function accessing a variable from its enclosing scope.

**Done when (step 1):** you can point at each variable in your script and say exactly which scope
it lives in and why.

**Step 2 — AI review pass:** ask the AI for a real bug caused by `var`'s function-scoping that
`let` would have prevented.

**Stretch (optional):** demonstrate the classic "loop variable captured by var vs let" bug with a
`setTimeout` inside a `for` loop.
