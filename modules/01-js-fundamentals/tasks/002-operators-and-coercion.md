# Task 002 — Operators and type coercion

**Concept:** `==` coerces types before comparing, `===` doesn't — most real JS bugs from
comparison come from not knowing which one you're using and why.

**Where this goes:** concept-lab — no project code here. The coercion judgment pays off in module
02, once you're comparing raw string values that come straight out of an HTML form input against
numbers/booleans and can't just trust `===`.

**Step 1 — build it yourself, no AI:** write 10 comparisons mixing types (`"5" == 5`, `0 ==
false`, `null == undefined`, `NaN === NaN`, etc.), predict each result on paper first, then run
and check.

**Done when (step 1):** you got at least 7/10 right *before* running them, and can explain the
ones you got wrong.

**Step 2 — AI review pass:** ask the AI to explain the coercion rule behind any prediction you got
wrong.

**Stretch (optional):** find out why `Number.isNaN(NaN)` is safer than `NaN === NaN`.
