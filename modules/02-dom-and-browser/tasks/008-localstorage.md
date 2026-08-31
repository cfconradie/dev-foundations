# Task 008 — localStorage

**Concept:** `localStorage` persists data in the browser across page reloads (unlike a JS
variable, which resets) — the simplest form of client-side persistence, and good practice for
"save state" before you have a real backend (module 04).

**Step 1 — build it yourself, no AI:** extend task 004's todo list to save its state to
`localStorage` on every change (add/toggle/remove) and load it back on page refresh, so the list
survives a reload.

**Done when (step 1):** reloading the page shows the same list state as before the reload,
including completed items.

**Step 2 — AI review pass:** ask the AI about localStorage's size limit and why it's unsuitable
for sensitive data (it's plain text, readable via devtools).

**Stretch (optional):** add a "clear all" button that also clears localStorage.
