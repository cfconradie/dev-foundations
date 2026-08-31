# Task 001 — Variables and types

**Concept:** `let`/`const`/`var` differ in scope and mutability, and JS has a small set of
primitive types plus objects — this is the vocabulary everything else is built from.

**Where this goes:** this is a concept-lab task, not project code — nothing you write here ends up
in the app. What it buys you: task 008 builds the real `PricingRule`/`QuoteRequest` objects, and
the moment you're deciding "is this field a string, a number, or a boolean," you're using the
judgment this task builds. If `typeof null` still surprises you by task 008, that's a sign to
come back here, not push through it.

**Step 1 — build it yourself, no AI:** in a scratch `.js` file run with `node` (not part of
`project/` — this is throwaway), declare a variable for each field a `PricingRule` needs (see
`PROJECT.md`'s data model) using the primitive type that actually fits it — a string for `name`, a
number for `priceDelta`, a boolean for whether it's a base option or an addon — log `typeof` each
one, and try reassigning a `const` to see the error. Before running, predict what `typeof null`
will print and write your guess down — most people guess wrong.

**Done when (step 1):** you can explain the difference between `let` and `const`, and whether your
`typeof null` prediction was right — and if it wasn't, you know why `"object"` is actually
considered a long-standing bug in the language, not a deliberate design choice.

**Step 2 — AI review pass:** tell the AI your `typeof null` prediction and whether it was right,
then ask: "Given that `typeof null === "object"`, show me a real bug this could cause in code that
checks `typeof someValue === "object"` to decide if it's safe to access a property on it — walk
through a specific value and a specific line of code that would break." Then ask a second
question, this one about where you're actually headed: "Task 008 will make `PricingRule` a real
object with these same fields — is there a type-choice mistake I could still make there that this
task wouldn't have caught?" Note both answers in `PROGRESS.md`.

**Stretch (optional):** look up what a Symbol and a BigInt are for.
