# Task 010 — Fetching data in React

**Concept:** combine custom hooks (task 007), `useEffect` (task 004), and `useState` (task 003)
into the admin quote-list view — the same feature you already built in Vue (module 06 task 009),
now in React.

**Step 1 — build it yourself, no AI:** build the `/admin` view: fetch all quote requests in
`useEffect`, render them in a Tailwind-styled table, and add a status-update action calling your
`PATCH` endpoint, updating local state on success.

**Done when (step 1):** the list loads real data and updates reflect immediately on status
change, matching the Vue version's behavior exactly.

**Step 2 — AI review pass:** ask the AI to check your PATCH error handling the same way you did
in Vue task 009 — did you handle the failure case as well this time, or is there regression?

**Stretch (optional):** add the same optimistic-update-with-rollback behavior you may have added
in Vue.
