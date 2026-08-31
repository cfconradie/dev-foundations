# Task 005 — Forms with v-model

**Concept:** `v-model` is two-way binding — it replaces the manual "read `.value` on input, write
back on change" pattern from module 02 with one directive.

**Step 1 — build it yourself, no AI:** rebuild your capstone's quote-request form (name, email)
using `v-model` on each input, with validation shown inline (reuse the validation logic from
module 02 task 005, don't rewrite it from scratch — this is a good case for an AI question about
reuse, but write the validation calls yourself).

**Done when (step 1):** the form validates and submits correctly, matching the vanilla-JS
version's behavior from the capstone.

**Step 2 — AI review pass:** ask the AI what `v-model` actually desugars to (a prop + an event) —
tie it back to task 003's props/events concept.

**Stretch (optional):** build a custom component that supports `v-model` itself.
