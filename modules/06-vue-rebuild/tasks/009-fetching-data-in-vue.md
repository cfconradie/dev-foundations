# Task 009 — Fetching data in Vue

**Concept:** combine everything so far — composables (task 007), lifecycle (task 006), computed
(task 004) — into the admin quote-list view fetching real data from your capstone backend.

**Step 1 — build it yourself, no AI:** build the `/admin` view: fetch all quote requests on
mount, render them in a table (Tailwind-styled), and add a status-update action calling your
`PATCH` endpoint, updating the UI reactively on success.

**Done when (step 1):** the list loads real data, and updating a status via the UI is reflected
immediately without a manual page refresh.

**Step 2 — AI review pass:** ask the AI to check your error handling for the PATCH call —
specifically what the UI does if the update fails partway (optimistic update gone wrong).

**Stretch (optional):** add optimistic UI updates with rollback on failure.
