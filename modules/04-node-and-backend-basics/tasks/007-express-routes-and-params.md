# Task 007 — Express routes and params

**Concept:** route params (`/products/:id`) and query strings (`?sort=price`) are how a REST API
receives specific identifiers and options — this is the vocabulary of every endpoint you'll write
from here on.

**Step 1 — build it yourself, no AI:** add `GET /api/products/:id` (returns one product by id
from an in-memory array, 404 if not found) and `GET /api/products?minPrice=X` (filters the array)
to your Express app from task 006.

**Done when (step 1):** both routes work correctly including the not-found case, and you can
explain the difference between a route param and a query string, and when to use each.

**Step 2 — AI review pass:** ask the AI whether your `:id` route correctly handles a
non-numeric id passed in the URL (e.g. `/api/products/abc`) without crashing the server.

**Stretch (optional):** add a nested route `GET /api/products/:id/reviews`.
