# Task 007 — Objects

**Concept:** objects are key-value collections with (usually) meaningful, non-sequential keys —
the shape you'll model almost everything in your app with (a user, a product, a form's state).

**Step 1 — build it yourself, no AI:** build a `product` object with nested data (e.g. a `specs`
sub-object and a `tags` array), then practice: dot notation vs bracket notation access, adding a
new key, deleting a key, checking a key exists with `in` and `hasOwnProperty`, and iterating keys
with `for...in` and `Object.keys/values/entries`.

**Done when (step 1):** you can access, mutate, and iterate the object using every method above
without looking any of them up mid-task.

**Step 2 — AI review pass:** ask when bracket notation is *required* (not just stylistic) over
dot notation.

**Stretch (optional):** deep-clone the object and prove the clone is independent (mutating one
doesn't affect the other).
