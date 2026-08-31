# Task 003 — CommonJS vs ES Modules

**Concept:** Node historically used `require`/`module.exports` (CommonJS); modern Node also
supports `import`/`export` (ESM, from module 01 task 019) — you'll meet both in real codebases, so
you need to recognize which one a project uses and why they can't be freely mixed.

**Step 1 — build it yourself, no AI:** write the same two-file module setup (a `math.js` +
`main.js`) twice: once using `require`/`module.exports`, once using `import`/`export` with
`"type": "module"` in `package.json`, and get both running.

**Done when (step 1):** both versions run correctly, and you can explain what
`"type": "module"` in `package.json` actually controls.

**Step 2 — AI review pass:** ask the AI what breaks if you try to `require()` an ESM-only package
from a CommonJS file, and why that's a common real-world dependency headache.

**Stretch (optional):** use dynamic `import()` inside a CommonJS file to load an ESM module.
