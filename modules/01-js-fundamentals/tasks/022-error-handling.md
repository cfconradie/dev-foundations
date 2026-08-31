# Task 022 — Error handling

**Concept:** `try/catch/finally` and throwing your own `Error` objects is how you handle things
going wrong on purpose instead of letting the program crash — critical once you touch APIs, user
input, or files.

**Where this goes:** concept-lab — this exact pattern (a clear custom error on bad input) is what
task 028's async submission handling wraps its `try/catch` around, and what module 04's real
backend routes will need for real user input.

**Step 1 — build it yourself, no AI:** write a `parseJSON(text)` function that wraps
`JSON.parse` in a `try/catch` and throws a clearer custom error message on failure; write a
`divide(a, b)` that throws on division by zero; call both with bad input and confirm the errors
are caught, not crashing the script.

**Done when (step 1):** both functions fail gracefully with a clear message for bad input, and
succeed normally for good input.

**Step 2 — AI review pass:** ask the AI when you should create a custom `Error` subclass instead
of throwing a plain `Error`, and whether your `finally` blocks (if any) are actually needed.

**Stretch (optional):** create a custom `ValidationError` class extending `Error`.
