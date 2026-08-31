# Task 003 — AAA pattern: testing pricing logic

**Concept:** Arrange/Act/Assert is a structure, not a style preference — Arrange sets up the exact
state a test needs, Act performs the one thing being tested, Assert checks one specific outcome.
A test that blurs these together is usually a test that's actually checking three things at once,
which is how you end up with a "passing" suite that still misses real bugs.

**Note:** this task is written to be self-contained since module 01 hasn't been retrofitted to
build the project's pricing logic yet (this is a pilot task from the course redesign — see
`modules/01.5-testing-fundamentals/README.md`). You'll write a small pricing function as part of
step 1, not import one from elsewhere.

**Step 1 — build it yourself, no AI:** using `PROJECT.md`'s `PricingRule` shape as your reference,
write a plain JS function `calculateTotal(selectedRuleIds, allRules)` that sums the price deltas
of the selected rules from a list of `PricingRule` objects (id, name, priceDelta, category). Set
up Vitest (`npm install -D vitest`, add a `test` script). Before writing any test code, write down
on paper or in a comment — in your own words — what you predict the function's behavior should be
for: (a) no rules selected, (b) one rule selected, (c) a selected id that doesn't exist in
`allRules`. Then write one AAA-structured test per case and run them.

**Done when (step 1):** three passing tests, each cleanly separated into Arrange/Act/Assert (as
either comments or blank-line sections), and your written predictions from before you wrote the
tests are still visible in your work (commit history or a comment) so step 2 can check them
against what you actually built.

**Step 2 — AI review pass:** paste your three tests and your pre-written predictions, and ask:
"Compare what I predicted case (c) should do against what my test actually asserts — do they
match, and if my implementation just silently ignores an unknown rule id instead of doing
something more defensible (like throwing or logging), is that a real bug I should fix or a
legitimate design choice? Argue it from what a real quote-calculator user would experience, not
in the abstract." Note the answer in `PROGRESS.md`.

**Stretch (optional):** add a fourth case — a rule with a negative `priceDelta` (a discount) — and
predict its behavior before testing it, same as the first three.
