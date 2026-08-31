# dev-foundations

A self-built course to go from zero formal CS background to a *thinking developer* — someone who
understands what the code does and can direct AI tools, not someone who just accepts whatever an
assistant generates ("vibe coding"). Tasks are sized to what each concept actually needs, not to a
fixed clock — some are quick, some need real room — and there's no fixed schedule; pull the next
one whenever you have time.

## The one rule: no-AI first, AI-review second

Every task has two steps:

1. **Build it yourself. No AI.** Use MDN / official docs / trial and error. Getting it wrong is
   fine and expected — that struggle is what builds understanding.
2. **AI review pass.** Once you have a working (or honestly-stuck) attempt, paste it to an AI and
   ask it to *critique*, not rewrite: what's wrong, what's fragile, what would a stronger engineer
   do differently, and to explain any concept you avoided or got wrong.

If you skip straight to asking AI to write the task for you, you've skipped the point of the
course. The AI's job here is code review and explanation, never generation.

## How to use a task

Open the next unchecked task in `PROGRESS.md`, read its file under `modules/<module>/tasks/`, do
step 1, do step 2, then tick it off and write one line in `PROGRESS.md` about what the AI review
taught you. That line matters more than the checkbox — it's the actual evidence you understood
something new. Each task also states, right after its "Concept," where it fits — either it builds
the running project directly, or it names the later task that will apply it for real.

## Structure

See `ROADMAP.md` for the full module list and the reasoning behind the order. Short version:

`HTML/CSS/Tailwind → project kickoff → JS fundamentals → testing fundamentals →
DOM/browser → data structures & algorithms → TypeScript → Node/backend → security fundamentals →
databases & SQL → capstone assembly/hardening → capstone rebuilt in Vue → capstone rebuilt in
React → system design & architecture → networking & delivery`

HTML/CSS is deliberately a short on-ramp, not the focus — Tailwind utility classes are used
throughout instead of hand-rolled CSS. The depth work is in JS/TS/Node, testing, DS&A, and
security: logic, types, data flow, architecture. Vue comes before React because Vue is more
transferable into React than the other way around, and by that point you already know the
underlying JS/TS concepts — you're only learning "how does this framework structure them," not the
language itself again.

## The running project

The course builds one project throughout, starting at module 00.5 — not disposable per-task
examples. `PROJECT.md` is the single source of truth for its spec and grows as modules add real
capability. It's a client-facing pricing/quote calculator: a real, deployable app shaped like the
kind of small custom-JS-logic job that actually gets hired for on Upwork — not a toy todo list. It
gets built once in vanilla JS/Node (assembled and hardened in module 05), then rebuilt in Vue, then
in React, so each framework is learned by solving the same real problem again rather than learning
syntax in the abstract. A few tasks (mostly generic algorithm drills and system-design case
studies) can't map onto it directly — those are tracked honestly in `INTEGRATION-BACKLOG.md` with
a planned tie-back, so nothing is a disconnected exercise without a stated purpose.
