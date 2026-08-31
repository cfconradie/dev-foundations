# Task 005 — Forms and validation

**Concept:** reading form input (`.value`), preventing the default full-page-reload submit
behavior, and validating before "submitting" is the exact shape of every real form you'll build,
frameworks included.

**Step 1 — build it yourself, no AI:** build a signup form (name, email, password) that calls
`event.preventDefault()` on submit, validates: name not empty, email contains `@`, password at
least 8 characters — showing an inline error message per invalid field instead of an alert.

**Done when (step 1):** submitting with bad data shows the right per-field errors and does not
reload the page; submitting with good data logs the clean data object.

**Step 2 — AI review pass:** ask the AI whether your email validation is reasonable for a
real app (full RFC email regex is usually overkill) and how it'd approach password strength
feedback.

**Stretch (optional):** disable the submit button while any field is invalid, re-enabling live as
the user types.
