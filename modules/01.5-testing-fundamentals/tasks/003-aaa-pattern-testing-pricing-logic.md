# Task 003 — AAA pattern: testing pricing logic

**Concept:** Arrange/Act/Assert is a structure, not a style preference — Arrange sets up the exact
state a test needs, Act performs the one thing being tested, Assert checks one specific outcome.
A test that blurs these together is usually a test that's actually checking three things at once,
which is how you end up with a "passing" suite that still misses real bugs.

**Where this goes:** project-track — this writes real tests against `project/pricing.js`'s real
`calculateTotal` (built in module 01, task 028), not a throwaway example.

**Note:** this is currently the only authored task in this module (a redesign pilot — see
`modules/01.5-testing-fundamentals/README.md`). Module 01 is fully authored, so `project/pricing.js`
should already exist with a real `calculateTotal(selectedRuleIds, allRules)` by the time you reach
this task — if it doesn't yet, do task 028 first.

**Step 1 — build it yourself, no AI:** set up Vitest (`npm install -D vitest`, add a `test`
script). Before writing any test code, write down — in your own words, as a comment or in
`PROGRESS.md` — what you predict `calculateTotal`'s actual behavior is, right now, for: (a) no
rules selected, (b) one rule selected, (c) a selected id that doesn't exist in the rules array.
Don't guess in the abstract — go read your own `project/pricing.js` implementation first, since
predicting the behavior of code you already wrote is the actual skill here, not predicting
behavior in general. Then write one AAA-structured test per case against the real function and run
them.

**Done when (step 1):** three passing tests against the real `calculateTotal`, each cleanly
separated into Arrange/Act/Assert (as either comments or blank-line sections), and your written
predictions from before you wrote the tests are still visible in your work (commit history or a
comment) so step 2 can check them against what you actually built.

**Step 2 — AI review pass:** paste your three tests, your pre-written predictions, and the actual
`calculateTotal` implementation, and ask: "Compare what I predicted case (c) should do against what
my test actually asserts and what the real implementation does — do all three agree, and if the
implementation just silently ignores an unknown rule id instead of doing something more defensible
(like throwing or logging), is that a real bug I should fix or a legitimate design choice? Argue it
from what a real quote-calculator user would experience, not in the abstract." Note the answer in
`PROGRESS.md`.

**Stretch (optional):** add a fourth case — a rule with a negative `priceDelta` (a discount) — and
predict its behavior before testing it, same as the first three.
