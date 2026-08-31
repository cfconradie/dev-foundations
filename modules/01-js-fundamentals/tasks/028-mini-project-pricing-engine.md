# Task 028 — Mini project: the project's real pricing engine (module capstone)

**Concept:** combine everything from this module — arrays/objects, array methods, closures,
recursion, `this`/classes, Maps, async, modules — into the project's actual pricing engine. This
isn't a practice exercise with throwaway data; what you build here is what module 02's UI will
call, what module 01.5's tests will cover, and what module 04's backend will eventually reuse. This
is the "can you actually build something real" checkpoint before moving into the DOM.

**Step 1 — build it yourself, no AI:** building on `pricing.js`/`format.js`/`main.js` from task
027, implement the project's real `calculateTotal(selectedRuleIds, allRules)` using the `Map`-based
lookup from task 010 (not a linear scan), a `makeDiscount(percent)` closure-based discount function
(from task 018's closures) applied to the subtotal, and — because a real pricing calculator often
has tiered/bundle discounts (buy 3+ addons, get an extra 10% off) — at least one piece of genuinely
recursive or nested logic from task 005's pattern, not forced in if it doesn't fit naturally.
Simulate the async "submit quote request" call with `await` + a fake delay that can succeed or
throw, handled with `try/catch` from task 022. Once it works end to end, update `PROJECT.md`'s
"Status" section to reflect that the pricing logic is real now, and add one changelog line.

**Done when (step 1):** running `main.js` against a real set of `PricingRule`s prints a correct
subtotal, discount, and total, a handled success/failure submission message, the logic is properly
split across modules, and `PROJECT.md` reflects the real state.

**Step 2 — AI review pass:** paste all three files and ask for an architecture review: is the
logic in the right file, is anything doing two jobs at once (e.g. is `calculateTotal` also doing
validation it shouldn't be responsible for), is error handling in the right place, and — since this
code will be directly reused by a real backend in module 04 — is there anything here that only
works because it's running in a trusted Node script and would need to change once untrusted user
input reaches it over HTTP? Log the single best suggestion in `PROGRESS.md`.

**Stretch (optional):** add a `promo code` feature via a second, composable discount function, and
note in `INTEGRATION-BACKLOG.md` (if you haven't already) that module 02.5's hash-map task will
revisit this exact `findRuleById` lookup for a real before/after performance comparison.
