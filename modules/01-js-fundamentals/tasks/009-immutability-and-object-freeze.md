# Task 009 — Immutability and `Object.freeze`

**Concept:** `const` stops you from *reassigning* a variable — it does nothing to stop you from
*mutating* the object that variable points to. That gap is a real, common source of bugs (a
function you pass an object into silently changes it), and `Object.freeze` is one real tool for
closing it — but it has a sharp edge worth knowing before you rely on it.

**Where this goes:** concept-lab — but this bug class is exactly what to watch for once task 028's
`calculateTotal` starts passing the same `PricingRule` array around; a function that accidentally
mutates shared rule data would be a real, hard-to-trace bug in the actual project.

**Step 1 — build it yourself, no AI:** take your `QuoteRequest` object from task 008. First, prove
`const` doesn't protect it: write a function `markContacted(quote)` that mutates `quote.status`
directly, call it, and confirm the original object changed even though it's `const`. Before
running the next part, predict: if you `Object.freeze()` a `QuoteRequest` that has a *nested*
`status` object, and then try to mutate `quote.status.value` (not the top-level `quote.status`
itself), will the freeze actually stop it? Write your prediction down, then test it.

**Done when (step 1):** you've demonstrated the `const`-doesn't-protect-you bug for real, and your
freeze prediction (right or wrong) is written down before you ran the test.

**Step 2 — AI review pass:** tell the AI your prediction and the actual result, then ask: "If my
prediction was wrong, walk through exactly why `Object.freeze` behaves the way it does with nested
objects, and show me the actual fix (not just 'freeze it deeper') that would make my whole
`QuoteRequest`, nested status included, genuinely immutable." Note the answer in `PROGRESS.md`.

**Stretch (optional):** implement the fix the AI review gave you and re-run your nested-mutation
test to confirm it now throws (in strict mode) or silently fails to change the value.
