# Task 010 — Connecting a database

**Concept:** an in-memory array (tasks 006-008) resets every server restart — a real database
persists data properly and is what separates a toy from a shippable app. SQLite (file-based,
zero setup) or Supabase (hosted Postgres, matches this account's existing stack) are both
reasonable choices here.

**Step 1 — build it yourself, no AI:** pick SQLite (`better-sqlite3`) or Supabase, create a
`products` table matching your task 003 (TS module) `Product` shape, and write a script that
inserts a few rows and reads them back, confirming the data survives a script restart.

**Done when (step 1):** data persists across separate script runs (proof it's not in-memory), and
you can explain, in plain terms, what a "connection string" or client config is doing.

**Step 2 — AI review pass:** ask the AI about SQL injection — show it a naive string-concatenated
query and ask it to demonstrate why a parameterized query prevents the attack.

**Stretch (optional):** add a second related table (e.g. `orders` referencing `products`) with a
foreign key.
