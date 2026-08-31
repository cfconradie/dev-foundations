# Task 003 — Conditionals

**Concept:** `if/else`, `switch`, and the ternary operator are three tools for the same job —
knowing when each reads clearer is a taste you build by using all three on the same problem.

**Where this goes:** concept-lab — no project code here. Task 028's real pricing engine has
genuine conditional logic (is a rule a base option or an addon, does a discount apply) — the
if/else-vs-ternary-vs-lookup judgment built here is what decides how that code reads.

**Step 1 — build it yourself, no AI:** write a function `classify(age)` that returns "child",
"teen", "adult", or "senior" — implement it three ways: `if/else`, `switch`, and nested ternaries.

**Done when (step 1):** all three versions return identical results for ages 5, 15, 30, 70.

**Step 2 — AI review pass:** ask which of your three versions is most readable and why, and
whether your `switch` used `break` correctly.

**Stretch (optional):** rewrite using an early-return style and compare readability.
