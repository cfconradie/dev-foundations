# Task 008 — Routing basics

**Concept:** Vue Router maps URLs to components client-side — your capstone needs at least two
"pages" (the public calculator, the admin quote list), and this is how a single-page app handles
that without a full page reload.

**Step 1 — build it yourself, no AI:** install Vue Router, set up two routes (`/` for the
calculator, `/admin` for the quote list), and add navigation between them.

**Done when (step 1):** navigating between routes doesn't reload the page, and the browser
back/forward buttons work correctly.

**Step 2 — AI review pass:** ask the AI to explain client-side vs server-side routing and why a
full page refresh on `/admin` might 404 without extra server config.

**Stretch (optional):** add a route param (`/admin/quotes/:id`) for a quote detail view.
