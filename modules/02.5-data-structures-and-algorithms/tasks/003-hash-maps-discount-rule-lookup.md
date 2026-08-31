# Task 003 — Hash maps: discount-rule lookup

**Concept:** a hash map trades a bit of memory for O(1) average-case lookup instead of an O(n)
scan — that's not just trivia, it's a real design decision with a measurable cost/benefit, and
"measurable" is the operative word: you should be able to prove the difference, not just assert it.

**Where this goes:** project-track — module 01 (task 010, task 028) already built
`project/pricing.js`'s `findRuleById` as a `Map`-based lookup, but that was built on faith, not
measured. This task is where you actually prove whether that choice was justified.

**Note:** this is currently the only authored task in this module (a redesign pilot — see
`modules/02.5-data-structures-and-algorithms/README.md`). Module 01 is fully authored, so
`project/pricing.js` should already exist with a real `Map`-based `findRuleById`.

**Step 1 — build it yourself, no AI:** the project's real rule set is small (a handful of pricing
options — check `PROJECT.md`), so measuring against it directly won't show anything: at that
scale, a linear scan and a `Map` lookup are both instant. To actually see the crossover point, you
need to stress-test past the project's real scale. Generate an array of 5,000 synthetic
`PricingRule` objects (id like `rule-0001`, a name, a `priceDelta`). Write a second, linear-scan
version of `findRuleById` (`.find()` or a manual loop) to compare against your real `Map`-based one
from `project/pricing.js` — don't rewrite the real one, import and reuse it. Before measuring
anything, write down your prediction: at what rough number of lookups do you expect the `Map`
version to clearly win, given that building the `Map` itself costs something up front? Then
actually measure both — run each version 10,000 times against the same 5,000-rule array and log
the total time for each with `console.time`/`console.timeEnd`.

**Done when (step 1):** you've measured your real `project/pricing.js` implementation against a
new linear-scan comparison, your before-measuring prediction is written down somewhere your commit
history preserves, and you have real timing numbers for both — not a guess, not "the Map one felt
faster."

**Step 2 — AI review pass:** paste both implementations and your actual timing numbers (not just
your prediction), and ask: "Given these specific numbers, was my prediction about the break-even
point right or wrong — and given that the project's real rule count is nowhere near where the
crossover happens, was building `findRuleById` as a `Map` in module 01 actually justified, or was
it premature optimization for data that'll never be large enough to need it? Argue it both ways,
then tell me which one you actually believe and why." Note the answer in `PROGRESS.md`, and add a
row to `INTEGRATION-BACKLOG.md` if the review surfaces something worth revisiting in
`project/pricing.js` itself.

**Stretch (optional):** repeat the measurement at 50 rules and 500,000 rules — does the break-even
point you predicted hold at both extremes, or does it shift?
