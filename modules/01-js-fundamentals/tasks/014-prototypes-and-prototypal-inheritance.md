# Task 014 — Prototypes and prototypal inheritance

**Concept:** every object in JS has a hidden link to another object (its prototype) that it falls
back to when a property lookup fails on the object itself — this is *how* `this` binding, method
lookup, and (next task) classes actually work under the hood. Skipping this means classes will
always feel like magic instead of syntax over something you understand.

**Step 1 — build it yourself, no AI:** without using `class`, build a `pricingRuleMethods` object
with one method, `describe()`, that returns a string using `this.name` and `this.priceDelta`.
Create two separate `PricingRule`-shaped objects using `Object.create(pricingRuleMethods)`, then
set `name`/`priceDelta` directly on each. Call `.describe()` on both and confirm it works even
though neither object has its own `describe` property. Before checking, predict: if you add a
*second* method to `pricingRuleMethods` *after* creating both rule objects, will the existing
objects be able to call it? Write your guess down, then test it.

**Done when (step 1):** both objects correctly inherit and use `describe()` via the prototype
chain (verify with `obj.hasOwnProperty('describe')` returning `false`), and your prediction about
adding a method after the fact is written down before you tested it.

**Step 2 — AI review pass:** tell the AI your prediction and the actual result, then ask: "Trace
exactly what JS does, step by step, when I call `.describe()` on one of these objects — where does
it look first, and where does it find the method? Then tell me what would happen if I'd also set a
`describe` property directly on one of the two rule objects — which one wins, and why?" Note the
answer in `PROGRESS.md`.

**Stretch (optional):** log `Object.getPrototypeOf(yourRuleObject) === pricingRuleMethods` to
confirm the link directly instead of just observing the behavior.
