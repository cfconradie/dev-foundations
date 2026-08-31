# dev-foundations

A self-built course to go from zero formal CS background to a *thinking developer* — someone who
understands what the code does and can direct AI tools, not someone who just accepts whatever an
assistant generates ("vibe coding"). Built for ~15-minute daily tasks, no fixed schedule — pull a
task whenever you have time.

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
something new.

## Structure

See `ROADMAP.md` for the full module list and the reasoning behind the order. Short version:

`HTML/CSS/Tailwind (light) → JavaScript fundamentals (the real depth work) → DOM/browser →
TypeScript → Node/backend → capstone app (vanilla) → same capstone rebuilt in Vue → same capstone
rebuilt in React`

HTML/CSS is deliberately a short on-ramp, not the focus — Tailwind utility classes are used
throughout instead of hand-rolled CSS. The depth work is in JS/TS/Node: logic, types, data flow,
architecture. Vue comes before React because Vue is more transferable into React than the other
way around, and by module 06 you already know the underlying JS/TS concepts — you're only
learning "how does this framework structure them," not the language itself again.

## Capstone

A client-facing pricing/quote calculator tool: a real, deployable app shaped like the kind of
small custom-JS-logic job that actually gets hired for on Upwork — not a toy todo list. Full spec
is in `modules/05-capstone-vanilla/README.md`. It gets built once in vanilla JS/Node, then rebuilt
in Vue, then in React, so each framework is learned by solving the same real problem again rather
than learning syntax in the abstract.
