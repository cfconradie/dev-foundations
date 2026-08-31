# Task 006 — Arrays basics

**Concept:** arrays are ordered, mutable, zero-indexed collections — most of your future data
manipulation (API responses, DOM lists, DB rows) comes back as arrays of objects, so this is
foundational.

**Where this goes:** concept-lab — no persisted project code yet, but this is real
`PricingRule`-shaped data, not an arbitrary example. Task 007 redoes this same problem
declaratively; task 028's real `calculateTotal` does the same summing for real.

**Step 1 — build it yourself, no AI:** build an array of 5 `PricingRule`-shaped objects (`{name,
priceDelta}`, per `PROJECT.md`), then without using higher-order array methods (no
`.map`/`.filter` yet — use loops), find the total price delta, find the most expensive rule, and
build a new array of just the names.

**Done when (step 1):** all three results are correct for a hardcoded 5-item array.

**Step 2 — AI review pass:** ask the AI to point out any place your loop-based code will be
replaced by a single array method in the next task, and why that's usually preferred.

**Stretch (optional):** handle an empty array without crashing.
