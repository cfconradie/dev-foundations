# Task 012 — Error handling and status codes (module capstone)

**Concept:** using the *correct* HTTP status code (400 vs 401 vs 404 vs 500) and a consistent
error response shape is what makes an API usable by a real client (including your future
Vue/React frontend) instead of guessing what went wrong from a 500 every time.

**Step 1 — build it yourself, no AI:** audit and fix every route from task 011 to return the
correct status code for its actual failure mode (400 for bad input, 404 for not found, 401 for
missing auth if you added it in task 008, 500 only for genuinely unexpected errors), using a
single centralized error-handling middleware (task 008 stretch) that formats all errors the same
way: `{ error: { message, code } }`.

**Done when (step 1):** every failure case in your CRUD API returns the correct status code and
the consistent error shape, verified for at least 5 distinct failure scenarios.

**Step 2 — AI review pass:** paste your whole API and ask for a final review before the capstone:
status code correctness, consistency of error shapes, and any missing validation. Log the
single most valuable finding — this is your last checkpoint before building the real capstone app.

**Stretch (optional):** add basic request logging that includes the response status code and
timing, so you can see this behavior in real time.
