# Task 011 — Browser devtools debugging

**Concept:** `console.log` is a blunt instrument — breakpoints, the call stack, watch
expressions, and the Network tab are how professional developers actually find bugs, including
bugs an AI's suggested fix didn't actually solve.

**Step 1 — build it yourself, no AI:** take a script from an earlier task with a subtle bug you
introduce on purpose (e.g. an off-by-one, a wrong comparison operator), then find it using ONLY
devtools breakpoints and step-through debugging — no `console.log` added. Use the Network tab to
inspect one of your earlier fetch requests/responses in detail.

**Done when (step 1):** you found and fixed the planted bug using breakpoints/step-through only,
and can point to the exact line and variable state that revealed it.

**Step 2 — AI review pass:** ask the AI for 2-3 devtools features you haven't used yet
(conditional breakpoints, `debugger;` statement, the Sources panel's watch panel) worth learning
next.

**Stretch (optional):** use the Performance tab to record and inspect a page load.
