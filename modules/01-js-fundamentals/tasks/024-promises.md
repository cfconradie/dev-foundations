# Task 024 — Promises

**Concept:** a Promise represents a value that will exist eventually (pending/fulfilled/rejected)
— it's the structured replacement for the nested callbacks from task 016, with `.then`/`.catch`
chaining instead of nesting.

**Step 1 — build it yourself, no AI:** rewrite task 016's `fetchUser` to return a `Promise`
instead of taking a callback, then rewrite the three-step chain using `.then()` chaining with a
single `.catch()` at the end. Also use `Promise.all` to fetch two independent things
concurrently.

**Done when (step 1):** the chained version produces the same result as task 016 but reads
top-to-bottom instead of nested, and `Promise.all` genuinely runs both fetches concurrently (log
timestamps to prove it).

**Step 2 — AI review pass:** ask the AI to check that your `.catch()` actually catches errors
from every step in the chain, not just the first.

**Stretch (optional):** implement `Promise.race` and explain when you'd use it over `Promise.all`.
