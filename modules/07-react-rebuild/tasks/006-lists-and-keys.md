# Task 006 — Lists and keys

**Concept:** rendering a list with `.map()` and a `key` prop is React's direct equivalent of
Vue's `v-for` + `:key` (module 06 task 002) — same underlying reason (helping the reconciler
track which item is which across re-renders), different syntax.

**Step 1 — build it yourself, no AI:** render your capstone's pricing-rule list with `.map()`,
using the rule's real id as the `key` (not the array index), then deliberately switch to using
the array index as the key while reordering the list to see the bug that causes (item state
getting mixed up).

**Done when (step 1):** you've reproduced the index-as-key bug, understand why it happens, and
reverted to using the stable id.

**Step 2 — AI review pass:** ask the AI to explain, at the reconciliation level, exactly why an
index key breaks when the list order changes but a stable id doesn't.

**Stretch (optional):** add/remove items from the list and confirm behavior stays correct with a
stable key.
