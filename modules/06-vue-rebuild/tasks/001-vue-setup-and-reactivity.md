# Task 001 — Vue setup and reactivity

**Concept:** Vue's `ref`/`reactive` replace the manual "update the DOM every time data changes"
work you did by hand in module 02 — this is the core trade you're making by using a framework.

**Step 1 — build it yourself, no AI:** scaffold a Vue 3 project (Vite), build a counter component
using `ref`, and compare it mentally to your module 01/02 manual counter — same behavior, far
less code because Vue re-renders automatically when the ref changes.

**Done when (step 1):** the counter works, and you can point to the exact line where you'd have
needed manual `.textContent` updates in vanilla JS that Vue's template binding replaced.

**Step 2 — AI review pass:** ask the AI to explain what "reactivity" means under the hood
(Proxies) at a level you can actually follow, not just "Vue tracks changes."

**Stretch (optional):** break reactivity on purpose (destructure a `reactive` object's property
directly) and see it stop updating, then fix it with `toRefs`.
