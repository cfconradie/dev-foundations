# Task 009 — Enums and literal types

**Concept:** an `enum` and a string-literal union (task 004) both model "one of a fixed set of
values" — TypeScript's own docs increasingly favor literal unions, so this task is as much about
knowing *why* as knowing the syntax.

**Step 1 — build it yourself, no AI:** model the same `OrderStatus` concept from task 004 twice:
once as a TS `enum`, once as a string-literal union, use both in equivalent functions, then look
up (in official TS docs, not AI) at least one concrete downside of enums that literal unions
don't have.

**Done when (step 1):** both versions work correctly, and you can state the specific downside you
found in your own words.

**Step 2 — AI review pass:** ask the AI to confirm or challenge the downside you found, and which
approach it would recommend for a new project today.

**Stretch (optional):** try a `const enum` and see how its compiled JS output differs from a
regular `enum`.
