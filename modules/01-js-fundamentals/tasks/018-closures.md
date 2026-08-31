# Task 018 — Closures

**Concept:** a closure is a function that "remembers" the variables from where it was created,
even after that outer function has returned — this is what makes counters, private state, and a
huge amount of real JS patterns (including React hooks later) work.

**Step 1 — build it yourself, no AI:** write a `makeCounter()` function that returns an object
with `increment`, `decrement`, and `getValue` methods, all sharing one private `count` variable
that can't be accessed directly from outside.

**Done when (step 1):** two separate calls to `makeCounter()` produce two independent counters,
and there is no way to read or set `count` except through the three methods.

**Step 2 — AI review pass:** ask the AI to explain, in terms of the call stack and memory, why
`count` isn't garbage-collected after `makeCounter()` returns.

**Stretch (optional):** build `makeCounter(step)` where each counter has its own custom
increment step.
