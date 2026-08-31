# Task 001 — Threat-model the project

**Concept:** a threat model isn't a checklist you fill in after the fact — it's asking, for one
specific system, "who would want to abuse this, and how" before you've been told the answer. Doing
it badly (guessing generic threats that could apply to any app) is easy; doing it well requires
actually looking at what *this* app exposes.

**Where this goes:** project-track — this becomes the findings doc later 04.5 tasks (and module
04's backend build) are checked against, not a standalone exercise.

**Step 1 — build it yourself, no AI:** re-read `PROJECT.md`'s user stories and architecture
section. No backend exists yet (module 04 hasn't happened), so you're threat-modeling the
*design*, not running code — that's a real skill: catching a security problem before you've written the
vulnerable line, not after. Write a list of at least 5 concrete threats, each in the form "an
attacker could [specific action] by [specific mechanism], which would let them [specific harm]" —
not "SQL injection is a risk," but e.g. "an attacker could submit a `QuoteRequest` with a script
tag in the `name` field, which would execute if the admin view renders it unescaped." Cover at
least: the public quote-submission form, the admin view, and the fact that there's no
authentication designed yet for that admin view.

**Done when (step 1):** at least 5 threats written in the specific form above, committed on your
task branch, covering all three areas listed.

**Step 2 — AI review pass:** paste your 5 threats and ask: "Given this project's actual
architecture (a public form, a database, an admin view with no designed authentication yet), what
threat did I miss that you'd flag as higher-priority than at least one of the 5 I found — and
argue specifically why it's higher priority for *this* app, not just 'it's a common vulnerability
in general.'" Note the answer in `PROGRESS.md`.

**Stretch (optional):** for your highest-priority threat, sketch (in words, no code yet) what the
fix would look like — you'll build it for real once modules 04/04.5's later tasks exist.
