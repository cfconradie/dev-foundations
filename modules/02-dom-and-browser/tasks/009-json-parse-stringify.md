# Task 009 — JSON.parse / JSON.stringify

**Concept:** `localStorage` only stores strings, and `fetch` bodies are strings too — `JSON.
stringify` (object → string) and `JSON.parse` (string → object) are the conversion you were
already using indirectly in tasks 006-008; this task makes it explicit and shows where it breaks.

**Step 1 — build it yourself, no AI:** stringify an object containing a nested array and a
`Date` object, parse it back, and compare the result to the original — specifically check what
happened to the `Date`. Then deliberately try to `JSON.parse` a malformed string and handle the
resulting error.

**Done when (step 1):** you can explain exactly what the `Date` object turned into after the
round trip and why, and the malformed-JSON case is caught, not crashing.

**Step 2 — AI review pass:** ask the AI what other JS values silently break or disappear in
`JSON.stringify` (hint: `undefined`, functions, `Symbol`).

**Stretch (optional):** use `JSON.stringify`'s second argument (a replacer function) to exclude
one field.
