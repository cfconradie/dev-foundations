# Task 010 — Maps and Sets

**Concept:** a plain object is fine for named fields, but when your keys are dynamic (an id you
don't know in advance) or you need guaranteed insertion order and any-type keys, `Map` is the
right tool — and `Set` is the equivalent for "a collection with no duplicates," which a plain
array can't guarantee without extra work.

**Step 1 — build it yourself, no AI:** you have an array of 5 `PricingRule` objects (see
`PROJECT.md`). Build a `Map` keyed by each rule's `id` so you can look one up directly instead of
scanning the array (module 02.5 comes back to *why* this matters for performance — for now, just
build it correctly). Separately, given an array of selected rule ids with an accidental duplicate
in it (a realistic bug — a UI double-click sent the same id twice), use a `Set` to deduplicate it
before computing a total, and prove the duplicate would have double-counted if you hadn't.

**Done when (step 1):** the `Map` correctly returns a rule by id in one lookup (no `.find()`), and
you can show a concrete before/after total proving the `Set` deduplication fixed a real
double-counting bug.

**Step 2 — AI review pass:** ask: "Given that a plain object can also be keyed by string ids, what
specifically would break or behave wrong if I'd used a plain object instead of a `Map` here — walk
through a concrete case, not just 'Map is more modern.'" Note the answer in `PROGRESS.md`.

**Stretch (optional):** convert your `Map` back to a plain array with `[...map.values()]` and
confirm you get the same 5 rules you started with.
