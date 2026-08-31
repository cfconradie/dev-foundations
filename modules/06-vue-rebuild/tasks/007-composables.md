# Task 007 — Composables

**Concept:** a composable is a reusable function that encapsulates stateful logic using Vue's
reactivity — the Vue equivalent of the closures pattern from module 01 task 011, now built for
component reuse.

**Step 1 — build it yourself, no AI:** extract your pricing-rule fetch + loading + error state
(task 006) into a `usePricingRules()` composable that any component can call, and use it in your
main component.

**Done when (step 1):** the component's own code shrinks to just calling the composable and using
its returned values, with identical behavior to before.

**Step 2 — AI review pass:** ask the AI when logic is "worth" extracting into a composable vs
when it's premature abstraction for a one-off use.

**Stretch (optional):** write a second composable, `useDebouncedRef`, using module 02 task 010's
debounce concept.
