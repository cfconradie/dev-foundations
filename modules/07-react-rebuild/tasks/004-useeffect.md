# Task 004 — useEffect

**Concept:** `useEffect` is React's version of Vue's lifecycle hooks (module 06 task 006) —
but unified into one hook controlled by a dependency array, which is the single most
commonly-misunderstood part of React for people coming from Vue.

**Step 1 — build it yourself, no AI:** fetch your capstone's pricing rules inside `useEffect`
with an empty dependency array (run once on mount, matching Vue's `onMounted`), then
deliberately remove the dependency array to see the infinite fetch loop, then fix it by adding
the array back and explain why the loop happened.

**Done when (step 1):** you've caused and fixed the infinite-loop bug on purpose, and can explain
in your own words what the dependency array controls.

**Step 2 — AI review pass:** ask the AI to explain the "stale closure inside useEffect" gotcha
(a variable referenced inside the effect not being in the dependency array) and check if your own
effect has this bug.

**Stretch (optional):** add a cleanup function (return a function from the effect) matching Vue's
`onUnmounted` from task 006.
