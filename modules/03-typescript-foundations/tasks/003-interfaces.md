# Task 003 — Interfaces

**Concept:** an `interface` describes the shape of an object — this is how you type the
`user`/`product` objects from module 01 so the compiler enforces the shape everywhere they're
used, catching typos and missing fields at compile time instead of runtime.

**Step 1 — build it yourself, no AI:** define a `Product` interface (name: string, price:
number, tags: string[], optional `discount?: number`), write a function `formatProduct(p:
Product)` that uses it, then deliberately pass an object missing a required field and read the
compiler error.

**Done when (step 1):** the compiler rejects the malformed object with a clear message pointing
at the missing field, and the optional field works both present and absent.

**Step 2 — AI review pass:** ask the AI the difference between `interface` and `type` for object
shapes, and when it actually matters which one you pick.

**Stretch (optional):** extend `Product` into a `DiscountedProduct` interface using `extends`.
