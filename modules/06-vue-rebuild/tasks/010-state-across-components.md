# Task 010 — State across components

**Concept:** once state (like selected pricing rules) needs to be shared across components that
aren't directly parent/child, prop-drilling (task 003) gets painful — a shared reactive store
(Pinia, or a simple composable-based store) solves this.

**Step 1 — build it yourself, no AI:** install Pinia (or build a minimal composable-based store
yourself first, then compare to Pinia) and move your capstone's selected-rules state into it, so
both the calculator display and a summary sidebar component read from the same source without
prop drilling.

**Done when (step 1):** both components stay in sync automatically, and you can explain why this
is preferable to passing the same state through multiple prop layers.

**Step 2 — AI review pass:** ask the AI when a shared store is overkill vs genuinely needed —
this app is small, so the honest answer might be "you didn't strictly need this," which is a
useful lesson itself.

**Stretch (optional):** persist the Pinia store's state to localStorage (module 02 task 008).
