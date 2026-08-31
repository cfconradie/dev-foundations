# Task 026 — The event loop

**Concept:** tasks 023–025 taught you callbacks, Promises, and async/await as three ways of
writing async code — but you've been trusting the *ordering* they produce without seeing the
mechanism that decides it. The event loop is that mechanism: one call stack, plus two queues
(microtasks for Promises, macrotasks for things like `setTimeout`), and the microtask queue always
fully empties before the next macrotask runs. That one rule explains a specific kind of ordering
surprise you're about to cause on purpose.

**Step 1 — build it yourself, no AI:** write this exact sequence and predict the console output
order *before* running it: `console.log("1")`, then `setTimeout(() => console.log("2"), 0)`, then
`Promise.resolve().then(() => console.log("3"))`, then `console.log("4")`. Write your predicted
order down. Then run it and compare. Once you understand why, extend it: add a second
`.then(() => console.log("5"))` chained off the same Promise, and a second `setTimeout(() =>
console.log("6"), 0)` — predict the full 6-line order again before running.

**Done when (step 1):** both predictions are written down before running, both were actually run,
and for any line you got wrong, you can explain which queue it was in and why that queue ran when
it did.

**Step 2 — AI review pass:** paste your two predictions (right or wrong) and the actual output,
and ask: "For the case I got wrong, trace it one step at a time through the call stack and both
queues — don't just restate the rule, walk through this exact code." Then ask a second, harder
question: "If I `await` inside an `async function`, which queue does the code *after* the `await`
resume on — and does that explain any ordering behavior I might have taken on faith in tasks
024/025 without actually checking?" Note the answer in `PROGRESS.md`.

**Stretch (optional):** add a synchronous loop that runs for a noticeable amount of time (e.g. a
tight loop to 100 million) between your first four `console.log`s and observe that it blocks
*everything* — including the "already resolved" Promise callback — until it finishes. This is the
concrete proof that JS is single-threaded.
