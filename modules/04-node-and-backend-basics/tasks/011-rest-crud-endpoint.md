# Task 011 — REST CRUD endpoint

**Concept:** combine Express routing (tasks 006-007) with the database from task 010 into a real
CRUD API (Create/Read/Update/Delete) — this is the shape of almost every backend endpoint you'll
ever write.

**Step 1 — build it yourself, no AI:** build full CRUD for `/api/products`: `GET` (list),
`GET /:id` (one), `POST` (create, validating the body), `PUT /:id` (update), `DELETE /:id` —
backed by your task 010 database, not an in-memory array.

**Done when (step 1):** all five operations work correctly via `curl` or a REST client, data
persists across server restarts, and invalid input to `POST`/`PUT` is rejected with a clear
error, not a crash.

**Step 2 — AI review pass:** paste your routes and ask for a review of validation coverage and
whether any route is vulnerable to bad input the AI can specifically demonstrate.

**Stretch (optional):** add pagination (`?page=`/`?limit=`) to the list endpoint.
