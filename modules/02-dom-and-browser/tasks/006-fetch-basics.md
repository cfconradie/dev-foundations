# Task 006 — Fetch basics

**Concept:** `fetch` makes an HTTP request from the browser and returns a Promise (module 01,
task 017) — this is how a page gets real data instead of hardcoded arrays, and it's the same API
you'll call from Vue/React later.

**Step 1 — build it yourself, no AI:** use `fetch` against a free public API (e.g.
`jsonplaceholder.typicode.com/users`) to get a list of users, then render their names into a
`<ul>` on the page using what you learned in task 002.

**Done when (step 1):** the page shows real data fetched at runtime, not hardcoded HTML, and you
can explain why you need `await response.json()` as a second step after `await fetch(url)`.

**Step 2 — AI review pass:** ask the AI why `fetch` doesn't reject on a 404/500 response (only on
network failure) and what that means for your error handling.

**Stretch (optional):** add a loading state shown while the fetch is in flight.
