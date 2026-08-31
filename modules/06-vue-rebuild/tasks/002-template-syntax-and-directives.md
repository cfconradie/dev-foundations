# Task 002 — Template syntax and directives

**Concept:** `{{ }}` interpolation, `v-if`/`v-show`, `v-for`, `v-bind`/`:` — this is Vue's
declarative replacement for the manual `createElement`/`classList` work from module 02.

**Step 1 — build it yourself, no AI:** render a list of your capstone's `PricingRule`s with
`v-for`, conditionally show a "no rules" message with `v-if`, and bind a Tailwind class
dynamically with `:class` based on whether a rule is selected.

**Done when (step 1):** the list renders from real data, the conditional message works, and the
class toggles correctly — with zero manual DOM manipulation code.

**Step 2 — AI review pass:** ask the AI the difference between `v-if` and `v-show` and which is
more appropriate for your "no rules" message.

**Stretch (optional):** add a `:key` to your `v-for` and ask the AI what breaks (subtly) if you
remove it.
