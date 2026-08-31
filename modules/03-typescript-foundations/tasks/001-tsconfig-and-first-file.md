# Task 001 — tsconfig and your first .ts file

**Concept:** `tsconfig.json` controls how strict the TypeScript compiler is — `strict: true` is
what makes TS actually useful (catches `null`/`undefined` bugs); without it you're barely getting
type-checking at all.

**Step 1 — build it yourself, no AI:** install TypeScript in a new project, create a
`tsconfig.json` with `strict: true`, write a trivial `.ts` file, and get it compiling/running
(`tsc` + `node`, or `ts-node`, or Vite).

**Done when (step 1):** the file compiles with zero errors, and you can explain what `strict:
true` turns on that matters (at minimum: `strictNullChecks`).

**Step 2 — AI review pass:** ask the AI to explain any tsconfig option you left at its default
without understanding it.

**Stretch (optional):** turn `strict` off, write code that would now compile but shouldn't, then
turn it back on and watch it fail.
