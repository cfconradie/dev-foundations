# Task 002 — Basic types

**Concept:** annotating `string`, `number`, `boolean`, arrays, and `any` — and understanding
exactly why `any` defeats the entire point of TypeScript — is the vocabulary everything else
builds on.

**Step 1 — build it yourself, no AI:** annotate variables of each primitive type, an array of
numbers, an array of strings, then deliberately type one variable as `any`, do something unsafe
with it (call a method that doesn't exist), and note that TypeScript doesn't catch it.

**Done when (step 1):** every properly-typed variable rejects an incorrect assignment (try one on
purpose and read the error), and you've seen firsthand how `any` lets a real bug through silently.

**Step 2 — AI review pass:** ask the AI when `any` is genuinely acceptable to use vs when
`unknown` is the safer choice for the same situation.

**Stretch (optional):** replace your `any` with `unknown` and see what extra checks TS now
forces you to add before using the value.
