# Task 006 — Narrowing

**Concept:** narrowing is how TypeScript lets you safely use a union type (task 004) or an
`unknown` value (task 002) — by checking it first (`typeof`, `instanceof`, `in`, or a custom type
guard) so TS "narrows" what it knows the value could be at that point in the code.

**Step 1 — build it yourself, no AI:** write a function accepting `string | number` that returns
a formatted version, using `typeof` narrowing to handle each case differently; then write a
custom type guard function `isProduct(x: unknown): x is Product` (using your task 003 interface)
and use it to safely handle an `unknown` value from a fake API response.

**Done when (step 1):** both functions compile with strict mode, and inside each narrowed branch
TS correctly restricts the type (hover/inspect to confirm, don't just trust it worked).

**Step 2 — AI review pass:** ask the AI to check whether your `isProduct` type guard actually
verifies enough fields to be safe, or if it would incorrectly accept a malformed object.

**Stretch (optional):** narrow a discriminated union (from task 004's stretch) using its shared
`type` field in a switch.
