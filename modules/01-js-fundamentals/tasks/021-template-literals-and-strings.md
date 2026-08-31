# Task 021 — Template literals and string methods

**Concept:** template literals (backticks) support interpolation and multi-line strings directly
— cleaner than string concatenation — and the common string methods (`slice`, `trim`, `split`,
`replace`, `includes`) are used constantly for formatting and parsing text.

**Step 1 — build it yourself, no AI:** build a multi-line "quote request received" email template
using a template literal, interpolating the visitor's name, their computed total (formatted as
currency, e.g. `$1,250`), and a list of their selected option names joined into one readable line.
Then write functions using string methods to: extract the domain from the visitor's submitted
email address, title-case their name for the template's greeting, and check whether their name
field accidentally contains a banned/placeholder value (e.g. "test", "asdf") a bad-faith or lazy
form submission might contain.

**Done when (step 1):** the email template renders correctly with a real `QuoteRequest`'s values,
and all three string-method functions pass on 3 test inputs each, including a deliberately bad one.

**Step 2 — AI review pass:** ask: "My domain-extraction function assumes the email has exactly
one `@` — walk through what a visitor could actually type into a quote-request form (not a
theoretical malformed string, an actual thing a real person or a bot would submit) that breaks
this assumption, and show me what my function currently does with it." Note the answer in
`PROGRESS.md`.

**Stretch (optional):** write a simple template-literal tag function that auto-escapes the
interpolated visitor name (defense against it later ending up in HTML — module 04.5 comes back to
why this specific habit matters).
