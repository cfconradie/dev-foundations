# Task 027 — Modules (import/export)

**Concept:** ES modules let you split code across files with explicit `export`/`import` instead
of one giant script — this is how every real project (including this one) is organized, starting
now.

**Where this goes:** this is a project-track task, not a concept-lab — `pricing.js`, `format.js`,
and `main.js` are the first real, persisted files in `project/`. Every module from here on builds
on these files directly instead of throwaway examples.

**Step 1 — build it yourself, no AI:** create a `project/` directory at the repo root if it
doesn't exist yet — this is where the app's real code lives from here on, separate from the
`modules/` task specs. Split your pricing logic into real files there that will keep growing as
the course continues: `project/pricing.js` with named exports (`calculateTotal`, the `Map`-based
`findRuleById` from task 010), `project/format.js` with a default export (`formatCurrency`,
pulling from task 021's currency formatting), and `project/main.js` that imports and uses both
against a small set of real `PricingRule` data. Before splitting, write down (one
sentence each) *why* you're putting each function in the file you chose — not just "it fits" —
since that's exactly the reasoning task 028's mini-project review will probe.

**Done when (step 1):** `main.js` runs correctly importing from both files, you can explain the
difference between a named export/import and a default export/import, and your one-sentence
reasoning for each file boundary is written down.

**Step 2 — AI review pass:** paste your file boundaries and your reasoning, and ask: "Given how
this project will keep growing (a real backend, real tests, a real UI all importing this same
pricing logic later), is `pricing.js`/`format.js` still the right split, or is there a boundary
here that'll become awkward once more code depends on it? Argue from the project's actual
trajectory, not general module-organization advice." Note the answer in `PROGRESS.md`.

**Stretch (optional):** re-export both from a third `index.js` barrel file and update `main.js` to
import from it instead.
