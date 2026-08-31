# Task 006 — Array methods (map/filter/reduce/find/sort)

**Concept:** `.map`, `.filter`, `.reduce`, `.find`, `.sort` are the loop-based logic from task 005
expressed declaratively — "what I want", not "how to iterate". This is the single most-used JS
skill in real code.

**Step 1 — build it yourself, no AI:** redo task 005's three answers using `.reduce` (total),
`.sort` + array access (most expensive), and `.map` (names array). Then add: `.filter` items over
$20, and `.find` the first item under $10.

**Done when (step 1):** every result matches task 005's loop-based answers, using zero manual
loops this time.

**Step 2 — AI review pass:** ask the AI to check your `.reduce` for correctness (a very common
place to get the initial value wrong) and whether your `.sort` comparator handles ties correctly.

**Stretch (optional):** chain three methods in one expression (`filter` → `map` → `reduce`).
