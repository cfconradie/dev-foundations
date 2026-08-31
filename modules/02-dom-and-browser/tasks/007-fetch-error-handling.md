# Task 007 — Fetch error handling

**Concept:** because of task 006's gotcha (fetch doesn't reject on HTTP error status), you must
manually check `response.ok`/`response.status` — this is one of the most commonly-missed bugs in
real apps.

**Step 1 — build it yourself, no AI:** rewrite task 006's fetch to check `response.ok`, throw a
descriptive error if not, wrap the whole thing in try/catch, and show a visible error message on
the page (not just a console log) for both a bad URL (network failure) and a valid-but-404 URL.

**Done when (step 1):** both failure types show a user-visible error message, and success still
renders the list correctly.

**Step 2 — AI review pass:** ask the AI to distinguish, in your code, which catch block is
handling a network failure vs an HTTP error status, and whether the user-facing messages should
differ.

**Stretch (optional):** add a retry button that re-runs the fetch on failure.
