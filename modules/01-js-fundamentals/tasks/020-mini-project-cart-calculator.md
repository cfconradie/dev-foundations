# Task 020 — Mini project: cart calculator (module capstone)

**Concept:** combine everything from this module — arrays/objects, array methods, functions,
closures, async, modules — into one working program. This is the "can you actually build
something" checkpoint before moving into the DOM.

**Step 1 — build it yourself, no AI:** build a Node script, split across modules (`cart.js`,
`pricing.js`, `main.js`), that: takes an array of `{name, price, qty}` items, applies a discount
function (closure-based: `makeDiscount(percent)` returns a function you apply to a total),
computes subtotal/discount/total using array methods, and simulates an async "checkout" call with
`await` + a fake delay that can succeed or throw.

**Done when (step 1):** running `main.js` prints a correct subtotal, discount, total, and a
handled success/failure checkout message, with the logic properly split across modules.

**Step 2 — AI review pass:** paste all three files and ask for an architecture review: is the
logic in the right file, is anything doing two jobs at once, is error handling in the right
place. Log the single best suggestion in PROGRESS.md.

**Stretch (optional):** add a `promo code` feature via a second, composable discount function.
