# Task 020 — Destructuring and spread/rest

**Concept:** destructuring pulls values out of arrays/objects by shape instead of by index/key
lookup, and spread/rest expand or collect values — together they're the syntax you'll see in
almost every modern JS/React/Vue codebase for passing data around, including the project's own
code from here on.

**Step 1 — build it yourself, no AI:** using your `QuoteRequest` object from task 008, destructure
`name` and `status.value` directly in one statement, renaming `name` to `visitorName` and giving
`status.value` a default of `"new"` in case it's missing; given the array of selected rule ids,
destructure the first selected rule's id and collect the rest with `...remainingRuleIds`; use
spread to build a new `QuoteRequest` that's a copy of the original with just `status` overridden
to `{ value: "contacted", updatedAt: new Date().toISOString() }` — this is the actual pattern
you'll use later to update a quote's status without mutating the original.

**Done when (step 1):** all three operations work against your real `QuoteRequest`, and you can
explain what "the rest" collects vs. what spread "expands".

**Step 2 — AI review pass:** ask: "Given my status-update spread pattern, what happens if
`status` itself is a nested object and I only spread the top-level `QuoteRequest` — does the
`status` object inside the copy share a reference with the original, or is it truly independent?
Show me a concrete mutation that would prove your answer." Note the answer in `PROGRESS.md`.

**Stretch (optional):** destructure function parameters directly (`function f({name, age}) {}`).
