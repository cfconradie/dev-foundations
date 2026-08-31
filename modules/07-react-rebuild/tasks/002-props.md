# Task 002 — Props

**Concept:** React props are the same "data down" concept as Vue props (module 06 task 003) —
passed as function arguments to a component function, since a React component *is* just a
function.

**Step 1 — build it yourself, no AI:** rebuild Vue task 003's parent/child pricing-rule-item
split in React, passing the rule as a prop and a callback function as a prop (React's replacement
for Vue's emitted events — there's no separate "emit" concept, it's just another prop).

**Done when (step 1):** clicking a child item updates the parent's state correctly, and you can
explain why React uses "pass a callback function as a prop" where Vue uses `emit`.

**Step 2 — AI review pass:** ask the AI to confirm this callback-prop pattern actually is
React's direct equivalent of Vue's emit, and if there's any meaningful difference beyond syntax.

**Stretch (optional):** type the component's props with a TS interface (module 03 task 003).
