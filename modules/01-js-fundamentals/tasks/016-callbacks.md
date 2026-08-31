# Task 016 — Callbacks

**Concept:** a callback is a function passed to run later — this is how JS handled async before
Promises existed, and understanding it (including "callback hell") is what makes you actually
appreciate why Promises and async/await exist.

**Step 1 — build it yourself, no AI:** write a `fetchUser(id, callback)` that uses `setTimeout`
to fake a 1-second network delay, then calls `callback(user)`. Chain three of these in sequence
(fetch user → fetch their orders → fetch order details) using nested callbacks only.

**Done when (step 1):** the three-step chain runs in the correct order and logs the final result,
using only callbacks (no Promises yet).

**Step 2 — AI review pass:** ask the AI to point out exactly where "callback hell" is starting to
appear in your nested code, and how deep it would get with two more steps.

**Stretch (optional):** add an error-first callback pattern (`callback(err, data)`).
