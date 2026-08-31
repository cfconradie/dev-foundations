# Task 003 — Hash maps: discount-rule lookup

**Concept:** a hash map trades a bit of memory for O(1) average-case lookup instead of an O(n)
scan — that's not just trivia, it's a real design decision with a measurable cost/benefit, and
"measurable" is the operative word: you should be able to prove the difference, not just assert it.

**Note:** this task is written to be self-contained since module 04 hasn't been retrofitted to
build the project's real backend/rule data yet (this is a pilot task from the course redesign —
see `modules/02.5-data-structures-and-algorithms/README.md`). You'll generate a synthetic rule
set as part of step 1.

**Step 1 — build it yourself, no AI:** generate an array of 5,000 synthetic `PricingRule` objects
(id like `rule-0001`, a name, a `priceDelta`) — a small script that builds them programmatically is
fine, this isn't the part being tested. Write two versions of a `findRuleById(id, rules)` lookup:
(1) a linear scan (`.find()` or a manual loop), (2) a version that first builds a `Map` keyed by
id, then looks up from the map. Before measuring anything, write down your prediction: at what
rough number of lookups do you expect the Map version to clearly win, given that building the Map
itself costs something up front? Then actually measure both — run each version 10,000 times
against the same 5,000-rule array and log the total time for each with `console.time`/`console.timeEnd`.

**Done when (step 1):** both implementations exist, your before-measuring prediction is written
down somewhere your commit history preserves, and you have real timing numbers for both — not a
guess, not "the Map one felt faster."

**Step 2 — AI review pass:** paste both implementations and your actual timing numbers (not just
your prediction), and ask: "Given these specific numbers, was my prediction about the break-even
point right or wrong, and why does the one-time cost of building the Map matter differently if
`findRuleById` gets called once per request versus once per app-startup? Which pattern actually
fits how a pricing calculator would call this function?" Note the answer in `PROGRESS.md`, and add
a row to `INTEGRATION-BACKLOG.md` noting that this technique is ready to apply to the project's
real discount-rule lookup once module 04's backend exists.

**Stretch (optional):** repeat the measurement at 50 rules and 500,000 rules — does the break-even
point you predicted hold at both extremes, or does it shift?
