# Task 013 — Destructuring and spread/rest

**Concept:** destructuring pulls values out of arrays/objects by shape instead of by index/key
lookup, and spread/rest expand or collect values — together they're the syntax you'll see in
almost every modern JS/React/Vue codebase for passing data around.

**Step 1 — build it yourself, no AI:** given a `user` object with nested `address`, destructure
`name` and `address.city` directly in one statement with renaming (`name: userName`) and a
default value for a missing field; given an array, destructure the first two items and collect
the rest with `...rest`; use spread to merge two objects with one field overridden.

**Done when (step 1):** all three destructuring/spread operations work and you can explain what
"the rest" collects vs what spread "expands".

**Step 2 — AI review pass:** ask the AI where destructuring can silently produce `undefined`
instead of an error, and why that matters for debugging.

**Stretch (optional):** destructure function parameters directly (`function f({name, age}) {}`).
