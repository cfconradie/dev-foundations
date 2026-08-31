# Task 008 — Objects

**Concept:** objects are key-value collections with (usually) meaningful, non-sequential keys —
the shape you'll model almost everything in your app with, including the project's real data.

**Step 1 — build it yourself, no AI:** using `PROJECT.md`'s data model, build a real
`QuoteRequest` object literal (name, email, an array of selected rule ids, a computed total, a
status, a timestamp) with the status nested one level deeper as `{ value: "new", updatedAt: null }`
so you have real nested data to practice on. Then practice: dot notation vs bracket notation
access, adding a new key (e.g. `notes`), deleting a key, checking a key exists with `in` and
`hasOwnProperty`, and iterating keys with `for...in` and `Object.keys/values/entries`.

**Done when (step 1):** you can access, mutate, and iterate the object using every method above
without looking any of them up mid-task, on your actual `QuoteRequest` object.

**Step 2 — AI review pass:** ask: "Given this exact `QuoteRequest` shape, show me one real
scenario where I'd be forced to use bracket notation instead of dot notation — not a made-up
example, one that could actually happen with this object's fields." Note the answer in
`PROGRESS.md`.

**Stretch (optional):** deep-clone the object and prove the clone is independent (mutating one
doesn't affect the other) — task 009 picks this exact problem back up from a different angle.
