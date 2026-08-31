# Task 010 — Utility types

**Concept:** `Partial`, `Pick`, `Omit`, `Readonly`, `Record` transform an existing type into a
new one instead of you retyping it by hand — a huge time-saver once your interfaces (task 003)
get real.

**Step 1 — build it yourself, no AI:** using your `Product` interface, build: a
`Partial<Product>` type used for an "update product" function that only requires changed fields,
a `Pick<Product, "name" | "price">` used for a summary card type, and a `Record<string, Product>`
used to model a lookup-by-id map.

**Done when (step 1):** all three derived types are used in a real function signature each, and
you can explain in one sentence what each utility type does without looking it up.

**Step 2 — AI review pass:** ask the AI for one utility type you didn't use (e.g. `Required`,
`Exclude`, `ReturnType`) that would be useful in this same codebase, and where.

**Stretch (optional):** use `ReturnType<typeof someFunction>` to derive a type instead of writing
it manually.
