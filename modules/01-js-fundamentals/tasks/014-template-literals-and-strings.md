# Task 014 — Template literals and string methods

**Concept:** template literals (backticks) support interpolation and multi-line strings directly
— cleaner than string concatenation — and the common string methods (`slice`, `trim`, `split`,
`replace`, `includes`) are used constantly for formatting and parsing text.

**Step 1 — build it yourself, no AI:** build a multi-line email template using a template
literal with 3 interpolated variables, then write functions using string methods to: extract a
domain from an email address, title-case a name, and check if a string contains a banned word.

**Done when (step 1):** the email template renders correctly with real values, and all three
string-method functions pass on 3 test inputs each.

**Step 2 — AI review pass:** ask the AI whether your domain-extraction function handles malformed
input (no `@`) gracefully.

**Stretch (optional):** write a simple template-literal tag function.
