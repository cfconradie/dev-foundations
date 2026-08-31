# Task 007 — Generics basics

**Concept:** a generic (`<T>`) lets a function or type work with any type while still being fully
type-checked — instead of writing `myMapNumbers`/`myMapStrings` separately, you write one
`myMap<T, U>` that works for both, matching your module 01 `myMap` implementation but now type-safe.

**Step 1 — build it yourself, no AI:** rewrite module 01's `myMap(array, fn)` as a generic
function `myMap<T, U>(array: T[], fn: (item: T) => U): U[]`, and use it once with numbers and once
with strings, confirming TS correctly infers the return type each time without you specifying
`<T, U>` explicitly.

**Done when (step 1):** both calls compile and infer correct types (hover to check), and passing
a mismatched function (e.g. one expecting a number to an array of strings) produces a compiler
error.

**Step 2 — AI review pass:** ask the AI to explain, in plain terms, what problem generics solve
that a plain `any`-typed function wouldn't — and get it to give you one real-world example beyond
`map`.

**Stretch (optional):** write a generic `firstOrDefault<T>(array: T[], fallback: T): T`.
