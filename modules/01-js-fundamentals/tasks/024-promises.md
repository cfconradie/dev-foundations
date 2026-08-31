# Task 024 — Promises

**Concept:** a Promise represents a value that will exist eventually (pending/fulfilled/rejected)
— it's the structured replacement for the nested callbacks from task 023, with `.then`/`.catch`
chaining instead of nesting.

**Where this goes:** concept-lab — the `Promise.all` concurrency pattern here is exactly what task
028's real project code uses, and what module 04's backend will use for concurrent DB/API calls.

**Step 1 — build it yourself, no AI:** rewrite task 023's `fetchUser` to return a `Promise`
instead of taking a callback, then rewrite the three-step chain using `.then()` chaining with a
single `.catch()` at the end. Also use `Promise.all` to fetch two independent things
concurrently.

**Done when (step 1):** the chained version produces the same result as task 023 but reads
top-to-bottom instead of nested, and `Promise.all` genuinely runs both fetches concurrently (log
timestamps to prove it).

**Step 2 — AI review pass:** ask the AI to check that your `.catch()` actually catches errors
from every step in the chain, not just the first.

**Stretch (optional):** implement `Promise.race` and explain when you'd use it over `Promise.all`.
