# Task 001 — JSX and components

**Concept:** JSX is JS with HTML-like syntax that compiles to function calls — unlike Vue's
templates (a separate syntax with directives), JSX is closer to "just write JS" with some sugar,
which is the single biggest structural difference between the two.

**Step 1 — build it yourself, no AI:** scaffold a React project (Vite), build the same counter
component from Vue task 001 using `useState`, and specifically notice: no `v-if`/`v-for`
directives — conditionals and loops are just JS expressions inside JSX (`{condition && <div/>}`,
`.map()`).

**Done when (step 1):** the counter works, and you can explain, using your own words, why React's
list rendering uses `.map()` (module 01 task 006) instead of a directive like `v-for`.

**Step 2 — AI review pass:** ask the AI to explain why JSX requires a `key` prop on list items,
tying it back to Vue's `:key` (module 06 task 002).

**Stretch (optional):** render a conditional using both `&&` and a ternary, and discuss which
reads clearer.
