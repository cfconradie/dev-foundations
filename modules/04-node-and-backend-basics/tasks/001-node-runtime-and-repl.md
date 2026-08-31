# Task 001 — Node runtime and REPL

**Concept:** Node is the JS engine (V8) plus APIs for filesystem/network/process that don't exist
in a browser (and browser APIs like `document` don't exist in Node) — knowing the boundary matters
for every "why doesn't this work" moment ahead.

**Step 1 — build it yourself, no AI:** open the Node REPL (`node` with no file), run a few
expressions interactively, then write a `.js` file that logs `process.version`,
`process.platform`, and `process.argv`, and run it passing a command-line argument.

**Done when (step 1):** you can read your own argument back from `process.argv`, and you can
name two things available in Node that aren't available in the browser (and vice versa).

**Step 2 — AI review pass:** ask the AI to list 3 more Node globals/APIs (beyond
`process`) worth knowing early.

**Stretch (optional):** use `process.exit(code)` with a non-zero code and check the exit code
from your shell (`echo $?`).
