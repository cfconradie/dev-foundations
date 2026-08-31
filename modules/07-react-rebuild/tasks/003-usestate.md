# Task 003 — useState

**Concept:** `useState` is React's version of Vue's `ref` (module 06 task 001) — but returns a
`[value, setter]` tuple (module 03 task 008) instead of a `.value`-accessed ref, and updates are
asynchronous/batched, which is a real, sometimes-surprising difference.

**Step 1 — build it yourself, no AI:** build your capstone's selected-rules state with
`useState`, then deliberately trigger the "stale closure" gotcha: call the setter twice in a row
using the current state variable directly (not the updater-function form) and observe it doesn't
double-update as naively expected; then fix it using the functional updater form
(`setState(prev => ...)`).

**Done when (step 1):** you've reproduced the bug, understood why it happens (closures again —
module 01 task 011), and fixed it correctly.

**Step 2 — AI review pass:** ask the AI to explain, precisely, why the functional updater form
fixes the bug you just reproduced — make sure the explanation matches what you actually observed.

**Stretch (optional):** reproduce the same class of bug with an object state update missing a
spread (`...prevState`).
