# Task 011 — Migrating a JS file to TypeScript

**Concept:** this is the real-world task you'll actually do most often — not writing TS from
scratch, but adding types to existing JS and fixing every compiler error that surfaces, each of
which is either a real latent bug or a place your original code was silently more permissive than
it should have been.

**Step 1 — build it yourself, no AI:** take module 01's task 020 mini-project (cart calculator)
and rename its files to `.ts`, add a `tsconfig.json` with `strict: true`, and fix every single
compiler error by adding proper types (interfaces for the cart items, types for the discount
functions) — no `any` allowed anywhere.

**Done when (step 1):** the project compiles with zero errors and zero `any`, and for at least
two of the errors you fixed, you can explain what real bug the untyped JS version could have hit
in production.

**Step 2 — AI review pass:** paste the final typed version and ask the AI to find any place where
a type is technically valid but still too loose (e.g. `price: number` that should really exclude
negatives via a branded type or a runtime check).

**Stretch (optional):** add a runtime validation function that checks untyped input (e.g. from
`JSON.parse`) actually matches your `CartItem` interface before trusting it.
