# Task 001 — Write the project charter

**Concept:** a spec written by someone who doesn't yet understand the problem is full of holes
they can't see — the only way to find those holes is to write the spec yourself first, then have
someone (or something) that wasn't in your head poke at it.

**Step 1 — build it yourself, no AI:** `PROJECT.md` at the repo root already has a seed spec for
the pricing/quote calculator (user stories, a rough data model, a target architecture). Read it,
then rewrite it in your own words — don't just leave the seed text in place. For each user story,
add one concrete example (real numbers, real option names) that shows exactly what it means. For
the data model, write out what you think `PricingRule` and `QuoteRequest` should actually contain
as plain JS-style object literals (you're not writing real code yet — this is module 01's job —
just sketch the shape). Commit this as your own artifact before moving to step 2.

**Done when (step 1):** `PROJECT.md`'s user stories each have a concrete example, the data model
sketch is in your own words with real example values, and you've committed it on your task branch
(see `modules/_workflow/git-workflow.md`).

**Step 2 — AI review pass:** paste your rewritten `PROJECT.md` section and ask: "Given these user
stories and this data model, walk through what happens when a visitor submits a quote request with
two conflicting options selected (e.g. two mutually-exclusive 'site type' choices) — does my spec
actually say what should happen, or did I leave a real case unhandled?" Don't accept a generic
answer — make the AI trace your specific data model, not spec-writing in general. Note the answer
in `PROGRESS.md`.

**Stretch (optional):** find a second unhandled edge case yourself (before asking AI) and see if
your own answer matches what the review surfaces.
