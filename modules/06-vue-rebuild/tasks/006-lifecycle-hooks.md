# Task 006 — Lifecycle hooks

**Concept:** `onMounted`, `onUnmounted`, etc. let you run code at specific points in a
component's life (e.g. "fetch data once the component exists") — the structured Vue equivalent of
"run this after the page loads" from module 02.

**Step 1 — build it yourself, no AI:** fetch your capstone's pricing rules from the backend
inside `onMounted` instead of at module load time, showing a loading state until they arrive
(reuse module 02 task 007's error-handling pattern).

**Done when (step 1):** the loading state shows correctly, and the rules render once fetched,
with errors handled visibly on failure.

**Step 2 — AI review pass:** ask the AI what `onUnmounted` is for, with a concrete example
relevant to this app (e.g. clearing a debounce timer, module 02 task 010).

**Stretch (optional):** add an `onUnmounted` cleanup for something in your app that actually
needs it.
