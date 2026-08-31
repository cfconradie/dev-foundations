# Task 005 — Recursion

**Concept:** a recursive function solves a problem by calling itself on a smaller version of the
same problem, with a base case that stops it — it's not a different tool from a loop, it's a
different way of expressing "repeat," and some real problems (walking nested data, the project's
own tiered pricing later in module 02.5) fit recursion far more naturally than a loop ever would.

**Step 1 — build it yourself, no AI:** rewrite task 004's Fibonacci-sequence generator
recursively (`fib(n)` returning the nth Fibonacci number, called in a loop to print the first 20).
Before measuring anything, predict in writing: will the recursive version be faster, slower, or
about the same speed as your task-004 loop version for the first 20 numbers? For the first 35?
Then actually measure both with `console.time`/`console.timeEnd` at both sizes.

**Done when (step 1):** both a working recursive `fib(n)` and your loop version from task 004
exist, your predictions are written down before you measured, and you have real timing numbers
for n=20 and n=35 — not a guess.

**Step 2 — AI review pass:** paste your recursive `fib` and your actual timing numbers, and ask:
"My recursive version got dramatically slower at n=35 than n=20 while the loop version barely
changed — walk through exactly why, in terms of how many times `fib` calls itself, and show me
what change (without switching back to a loop) would fix it." Note the answer — and whether your
prediction was right — in `PROGRESS.md`.

**Stretch (optional):** implement the fix the AI review suggested (likely memoization) and
re-measure n=35 to confirm it actually closed the gap.
