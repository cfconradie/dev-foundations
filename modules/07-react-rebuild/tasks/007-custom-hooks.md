# Task 007 — Custom hooks

**Concept:** a custom hook is React's version of a Vue composable (module 06 task 007) — a
reusable function encapsulating stateful logic, following the same closure-based pattern from
module 01.

**Step 1 — build it yourself, no AI:** extract your pricing-rule fetch + loading + error state
into a `usePricingRules()` custom hook, matching the Vue composable you wrote in module 06, and
compare the two files side by side.

**Done when (step 1):** the component using the hook is as clean as the Vue version was, and you
can list, concretely, what's identical between the composable and the custom hook and what's
purely syntactic difference.

**Step 2 — AI review pass:** ask the AI if there's any *meaningful* (not just syntactic)
difference between a Vue composable and a React custom hook — most people assume they're
identical; check if that's actually true.

**Stretch (optional):** write `useDebouncedValue`, matching module 02 task 010's debounce.
