# Task 005 — Forms and controlled inputs

**Concept:** React has no `v-model` — a "controlled input" (value from state + onChange setting
state) is the manual version of what Vue does for you automatically, which is a genuinely useful
thing to feel by hand once.

**Step 1 — build it yourself, no AI:** rebuild your capstone's quote-request form in React using
controlled inputs (`value={state}` + `onChange={e => setState(e.target.value)}` for each field),
reusing your existing validation logic.

**Done when (step 1):** the form behaves identically to the Vue version, and you can explain,
concretely, what extra code React required here that Vue's `v-model` did for you.

**Step 2 — AI review pass:** ask the AI whether a reusable custom hook (task 007) would reduce
the repetition across your form's multiple controlled inputs.

**Stretch (optional):** build a `useFormField` custom hook and refactor the form to use it.
