# Task 004 — Loops

**Concept:** `for`, `while`, and `for...of` solve "repeat until X" differently — picking the right
one for the data you have (an index range vs an iterable) is the actual skill.

**Where this goes:** concept-lab — Fibonacci is a pure mechanics exercise, not project code. Task
006, immediately next, starts looping over real `PricingRule` data, so this fluency pays off one
task later, not in this one.

**Step 1 — build it yourself, no AI:** print the first 20 Fibonacci numbers three ways: a classic
`for` loop, a `while` loop, and a `for...of` over a pre-built array — then write a loop that skips
multiples of 3 using `continue` and stops early using `break`.

**Done when (step 1):** all three Fibonacci versions produce the same 20 numbers, and you can
explain when you'd reach for `for...of` over a classic `for`.

**Step 2 — AI review pass:** ask if any of your loops could cause an off-by-one error and why.

**Stretch (optional):** none — task 005 picks this exact problem back up recursively and asks you
to measure the difference for real.
