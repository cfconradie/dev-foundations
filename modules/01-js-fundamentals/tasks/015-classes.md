# Task 015 — Classes

**Concept:** `class` is syntax over exactly the prototype mechanism from task 014 — a
constructor function plus methods living on the prototype, written in a shape that looks like
classical OOP. Knowing that means you never have to wonder "but what is a class *actually*
doing" — you already built the underlying mechanism by hand last task.

**Where this goes:** concept-lab — same honesty as task 014: the project ends up typing
`PricingRule`/`DiscountRule` as plain objects with a discriminated union in module 03, not
classes. This task's payoff is that "what is a class actually doing" is no longer a mystery, not
project code you'll reuse verbatim.

**Step 1 — build it yourself, no AI:** rewrite task 014's `Object.create`-based `PricingRule` as a
real `class PricingRule` with a constructor (`name`, `priceDelta`) and a `describe()` method.
Then create a `class DiscountRule extends PricingRule` that adds a `percentOff` field and
overrides `describe()` to call `super.describe()` and append the discount info. Before running,
predict: will `new DiscountRule(...) instanceof PricingRule` be `true` or `false`? Write it down,
then test it.

**Done when (step 1):** both classes work, `DiscountRule.describe()` correctly includes the
`super.describe()` output plus its own addition, and your `instanceof` prediction is written down
before testing.

**Step 2 — AI review pass:** ask: "Show me, using `Object.getPrototypeOf`, that `DiscountRule`'s
prototype chain is built exactly the way task 014's manual `Object.create` version was — prove
`class` didn't invent a new mechanism, it's the same prototype chain with different syntax." Note
the answer in `PROGRESS.md`.

**Stretch (optional):** add a `static` method to `PricingRule` (e.g. `PricingRule.compare(a, b)`
for sorting) and explain why it's not available on instances.
