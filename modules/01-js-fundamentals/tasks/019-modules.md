# Task 019 — Modules (import/export)

**Concept:** ES modules let you split code across files with explicit `export`/`import` instead
of one giant script — this is how every real project (including your capstone) is organized.

**Step 1 — build it yourself, no AI:** split your module 01 work into files: a `math.js` with
named exports (`sum`, `average`), a `format.js` with a default export (`formatPrice`), and a
`main.js` that imports and uses both (run with Node's ESM support or a Vite dev server).

**Done when (step 1):** `main.js` runs correctly importing from both files, and you can explain
the difference between a named export/import and a default export/import.

**Step 2 — AI review pass:** ask the AI when named exports are preferred over default exports in
real projects, and why.

**Stretch (optional):** re-export something from `math.js` through a third `index.js` barrel file.
