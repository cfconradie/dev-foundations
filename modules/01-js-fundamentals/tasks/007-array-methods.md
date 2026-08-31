# Task 007 — Array methods (map/filter/reduce/find/sort)

**Concept:** `.map`, `.filter`, `.reduce`, `.find`, `.sort` are the loop-based logic from task 006
expressed declaratively — "what I want", not "how to iterate". This is the single most-used JS
skill in real code.

**Where this goes:** concept-lab — task 010's Map-based rule lookup and task 028's real
`calculateTotal` both lean directly on `.reduce`/`.find` over `PricingRule` arrays; this is where
that fluency gets built.

**Step 1 — build it yourself, no AI:** redo task 006's three answers using `.reduce` (total),
`.sort` + array access (most expensive), and `.map` (names array). Then add: `.filter` rules over a
$20 price delta, and `.find` the first rule under $10.

**Done when (step 1):** every result matches task 006's loop-based answers, using zero manual
loops this time.

**Step 2 — AI review pass:** ask the AI to check your `.reduce` for correctness (a very common
place to get the initial value wrong) and whether your `.sort` comparator handles ties correctly.

**Stretch (optional):** chain three methods in one expression (`filter` → `map` → `reduce`).
