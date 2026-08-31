# Task 008 — Middleware

**Concept:** middleware is a function that runs on every (or matching) request before your route
handler — logging, auth checks, and body parsing (task 006's `express.json()`) are all just
middleware, and once you write your own, the pattern stops being magic.

**Step 1 — build it yourself, no AI:** write your own middleware function (not from a library)
that logs the method, URL, and timestamp of every request, register it with `app.use()`, then
write a second middleware that checks for a fake `Authorization` header and returns 401 if
missing, applied only to your `/api/products` routes.

**Done when (step 1):** every request logs correctly, and hitting `/api/products` without the
header returns 401 while other routes still work.

**Step 2 — AI review pass:** ask the AI to explain the role of `next()` in your middleware and
what happens (hangs forever) if you forget to call it.

**Stretch (optional):** write error-handling middleware (4-arg signature) that catches thrown
errors from any route.
