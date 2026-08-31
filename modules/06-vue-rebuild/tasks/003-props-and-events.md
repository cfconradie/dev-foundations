# Task 003 — Props and events

**Concept:** components pass data down via props and communicate back up via emitted events —
the structured version of what plain functions/callbacks (module 01) were already doing, now
scoped to component boundaries.

**Step 1 — build it yourself, no AI:** split your pricing-rule list into a parent and a
`PricingRuleItem` child component, passing the rule as a prop and emitting a `toggle` event when
clicked, handled by the parent.

**Done when (step 1):** clicking a child item updates the parent's selection state correctly, and
you can explain why the child shouldn't mutate the prop it received directly.

**Step 2 — AI review pass:** ask the AI to name the "props down, events up" principle and why
Vue (and React later) enforce it.

**Stretch (optional):** add prop type validation (`defineProps<{...}>()` in TS).
