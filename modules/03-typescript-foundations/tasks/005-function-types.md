# Task 005 — Function types

**Concept:** typing a function's parameters and return value — including optional/default
parameters and typing a callback parameter itself — is what lets TS catch you calling a function
wrong before you ever run it.

**Step 1 — build it yourself, no AI:** type module 01's `sum(...numbers)` and `formatPrice(amount,
currency = "USD")` fully (parameters and return type), then write a higher-order function
`applyDiscount(amount: number, discountFn: (n: number) => number): number` and pass it two
different typed discount functions.

**Done when (step 1):** all functions are fully typed with no `any`, and calling any of them with
a wrong-typed argument produces a compiler error you can explain.

**Step 2 — AI review pass:** ask the AI whether your return type annotations are actually needed
here or if TS's inference already got them right — and when explicit return types matter more (
public APIs/exported functions).

**Stretch (optional):** type a function that can return two different shapes based on an input
flag (an overload or a union return type).
