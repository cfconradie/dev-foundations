# Task 012 — Mini project: typed cart API shape (module capstone)

**Concept:** model a small but realistic typed data layer — the exact kind of thing you'll build
for real in module 04's backend and reuse in the capstone.

**Step 1 — build it yourself, no AI:** design and fully type (interfaces + unions, no `any`): a
`Product`, a `CartItem` (product + quantity), a `Cart` (items + computed totals), an `OrderStatus`
union, and an `Order` (cart + status + timestamp). Write typed functions to add an item to a cart,
compute the cart total, and transition an order to the next valid status (rejecting invalid
transitions using narrowing).

**Done when (step 1):** every function and data shape is fully typed with strict mode on, and
attempting an invalid status transition is caught at compile time or runtime (your choice, but
you must be able to explain which and why).

**Step 2 — AI review pass:** paste the full type definitions and ask for a review focused
specifically on typing decisions: anything too loose, anything over-engineered for the problem
size, and whether the status-transition logic is modeled well. Log the best finding.

**Stretch (optional):** model the "invalid transition" as a proper typed error rather than a
generic throw.
