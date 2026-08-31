# Task 025 — Async/await

**Concept:** `async/await` is syntax sugar over Promises that lets async code read like
synchronous code — same underlying mechanism as task 024, easier to follow, and what you'll use
almost everywhere afterward.

**Where this goes:** concept-lab — this is the exact syntax task 028's real "submit quote request"
simulation uses, and what module 04's real backend routes are written in throughout the rest of
the course.

**Step 1 — build it yourself, no AI:** rewrite task 024's `.then()` chain as an `async function`
using `await`, with a `try/catch` for error handling instead of `.catch()`. Then rewrite the
`Promise.all` concurrent fetch using `await Promise.all([...])`.

**Done when (step 1):** the async/await version produces identical output to the Promise-chain
version, and you can explain in one sentence why `await` only works inside an `async` function.

**Step 2 — AI review pass:** ask the AI to check whether you accidentally made two independent
`await` calls sequential when they could have run concurrently with `Promise.all` — this is one
of the most common real-world performance bugs.

**Stretch (optional):** add a timeout using `Promise.race` between your async call and a
rejecting timer.
