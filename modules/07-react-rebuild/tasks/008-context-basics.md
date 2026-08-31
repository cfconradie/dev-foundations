# Task 008 — Context basics

**Concept:** React Context is the equivalent of a shared store (Vue's Pinia, module 06 task 010)
for state that needs to reach components without prop drilling — though for anything beyond
simple shared state, most real projects still reach for a dedicated store library.

**Step 1 — build it yourself, no AI:** move your capstone's selected-rules state into a Context
provider, and consume it from two sibling components (the calculator display and a summary
sidebar) without prop drilling, matching what you built in Vue with Pinia.

**Done when (step 1):** both components stay in sync, and you can explain one real downside of
Context for frequently-changing state (unnecessary re-renders of every consumer).

**Step 2 — AI review pass:** ask the AI when it would recommend a dedicated state library
(Zustand, Redux) over Context for this exact app, and why.

**Stretch (optional):** split the context into two (state + dispatch) to reduce unnecessary
re-renders.
