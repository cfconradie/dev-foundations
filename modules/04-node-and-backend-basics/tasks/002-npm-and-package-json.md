# Task 002 — npm and package.json

**Concept:** `package.json` declares your project's dependencies and scripts; `npm install`
resolves them into `node_modules`; understanding this is what makes every "just run npm install"
instruction make sense instead of being a magic incantation.

**Step 1 — build it yourself, no AI:** run `npm init -y` in a new folder, install one real
dependency (e.g. `chalk` or `dayjs`) and one dev dependency (e.g. `nodemon`), add a `"dev"` script
to `package.json` that runs your entry file with nodemon, and use the installed package in code.

**Done when (step 1):** `npm run dev` restarts your script automatically on file save, and you
can explain the difference between `dependencies` and `devDependencies` in `package.json`.

**Step 2 — AI review pass:** ask the AI to explain semantic versioning (`^1.2.3` vs `~1.2.3` vs
exact) as it appears in your own `package.json`.

**Stretch (optional):** check in a `package-lock.json`, delete `node_modules`, and reinstall from
lockfile only — confirm versions match exactly.
