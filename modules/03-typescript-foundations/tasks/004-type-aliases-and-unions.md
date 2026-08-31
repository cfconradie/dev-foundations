# Task 004 — Type aliases and unions

**Concept:** a `type` alias can name any type, including a union (`"pending" | "shipped" |
"delivered"`) — this is how you model "one of a few specific values" far more safely than a plain
`string`.

**Step 1 — build it yourself, no AI:** define a union type `OrderStatus` with 3-4 specific string
values, write a function `describeStatus(status: OrderStatus)` using a `switch` that handles every
case, then try passing an invalid string literal and read the compiler error.

**Done when (step 1):** the compiler rejects any string not in the union, and your `switch`
handles all defined cases (try removing one case and see if TS's exhaustiveness checking catches
it, if configured).

**Step 2 — AI review pass:** ask the AI how to make the switch statement's exhaustiveness
actually enforced by the compiler (the `never` type trick) if your first pass didn't already do
this.

**Stretch (optional):** add a union of object shapes (a "discriminated union") for two different
notification types sharing a `type` field.
