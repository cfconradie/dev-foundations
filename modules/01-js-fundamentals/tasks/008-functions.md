# Task 008 — Functions

**Concept:** function declarations, function expressions, default parameters, and rest
parameters are the vocabulary of "reusable logic" — get comfortable with all the shapes before
arrow functions add another one.

**Step 1 — build it yourself, no AI:** write a `formatPrice(amount, currency = "USD")` function
using a function declaration, then rewrite it as a function expression assigned to a `const`, then
write a `sum(...numbers)` using rest parameters.

**Done when (step 1):** both `formatPrice` versions behave identically including the default
parameter, and `sum()` works for any number of arguments including zero.

**Step 2 — AI review pass:** ask the AI to explain hoisting — why the declaration version can be
called before its definition in the file but the expression version can't.

**Stretch (optional):** make `formatPrice` throw a clear error for a negative amount.
