# Task 004 — File system basics

**Concept:** Node's `fs` module reads/writes files — the server-side equivalent of
`localStorage` (module 02, task 008), and the first "real" server capability you'll use before a
database.

**Step 1 — build it yourself, no AI:** write a script that reads a JSON file of products (create
one by hand), parses it (module 01 task 009), adds a new product, and writes it back to disk —
using the `fs/promises` API with `async/await`, not callbacks.

**Done when (step 1):** running the script twice shows the file growing by one product each
time, and you can explain why you used the promise-based `fs` API instead of the callback-based
one.

**Step 2 — AI review pass:** ask the AI about the race condition risk if two requests write to
the same file concurrently — this is exactly why real apps use a database instead.

**Stretch (optional):** add file-existence checking so the script creates the file with an empty
array if it doesn't exist yet.
