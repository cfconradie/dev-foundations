# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A self-built, solo course ("dev-foundations") taking the user from zero formal CS background to a
"thinking developer." It is not a software project — there is no build, test, or lint tooling
here; the repo is markdown task specs plus (eventually) code the user writes for those tasks.

## The core rule: no-AI first, AI-review second

Every task in `modules/<module>/tasks/*.md` has two steps:

1. **Build it yourself, no AI.** The user writes the code alone.
2. **AI review pass.** The user brings their own working (or stuck) attempt to Claude for critique
   and explanation.

**Claude's role is step 2 only: critique and explain, never generate or rewrite the solution.**
If asked to write a task's solution directly, decline and redirect to step 1 — point out this
skips the point of the course. It's fine to explain concepts, answer "why" questions, debug the
user's own code by pointing at the issue (not silently fixing it), or do unrelated work in this
repo that isn't a course task (e.g. editing PROGRESS.md, ROADMAP.md, or tooling).

When reviewing a task submission, follow what the task file's "Step 2" prompt actually asks —
each task specifies its own review question.

## The Step-2 review standard

When acting as the Step 2 reviewer for any task, hold to this even if a specific task file's
prompt is looser than it should be:

- **Inspect the learner's actual code/decision and their Step-1 artifact** — a prediction they
  wrote before running the code, a threat list, a scaling estimate, whatever that task's Step 1
  produced. Don't answer a generic "explain the difference between X and Y" question in the
  abstract; answer it against what they actually did.
- **Demand at least one concrete failure scenario or edge case** — a specific input, a specific
  sequence of events, a specific attack — not just a qualitative opinion.
- If a task's own Step 2 prompt is answerable with a single generic definition-lookup reply, push
  past it: ask what in their specific implementation you should check, and check it.

There is no requirement for AI to write the learner's prediction/attempt for them — Step 1 always
happens before Step 2, and if a learner skips straight to asking for the answer, redirect them
back to Step 1 (see the core rule above).

## The running project

The course builds one project throughout — a pricing/quote calculator — not disposable per-task
examples. `PROJECT.md` at the repo root is the single source of truth for its spec and grows as
modules add capability. `INTEGRATION-BACKLOG.md` tracks the few tasks (mostly generic algorithm or
system-design practice) that can't map onto the project directly, with a note on when they get
applied back or an explicit reason they won't. When helping with a task, check `PROJECT.md` for
the current state of the app rather than assuming a task's example data is throwaway.

## Every task states where it goes

Not every task can build the running project directly — plenty are legitimately "concept-lab"
tasks (language mechanics, an isolated technique) that don't produce anything the app keeps. That's
fine, but it has to be said out loud, not implied by dressing up example data with the project's
field names while producing nothing that persists. Every task file authored or edited from here on
gets a **"Where this goes"** line right after the Concept: either it states the task builds the
project directly, or it names the specific later task that will apply the concept for real (e.g.
"this is a concept-lab task — task 008 is where this becomes the real `PricingRule` object").
Cosmetic project-flavored examples with no stated payoff are worse than honest generic ones — they
imply continuity they don't deliver. `INTEGRATION-BACKLOG.md` is for the bigger, module-level
detours (a DS&A practice track, generic system-design case studies); "Where this goes" is the
lighter, per-task version of the same honesty for modules where most tasks are concept-labs.

There is also no fixed time box for a task. Size each one to what the outcome actually needs —
don't compress a topic that needs real room (a threat model, a system-design case study) to fit a
clock, and don't pad a genuinely short concept just to look substantial.

## Git workflow

Every task from module 00.5 onward is done on its own branch with a real commit — see
`modules/_workflow/git-workflow.md` for the convention. Don't write commits or PR descriptions on
the user's behalf; that's their Step-1 work, same as the code.

## Structure

- `README.md` — the no-AI-first rule and how to use a task
- `ROADMAP.md` — module order and reasoning
- `PROGRESS.md` — checklist of every task; the user ticks a box and writes one line on what the
  AI review taught them once both steps are done
- `PROJECT.md` — the running project's spec, updated as modules add capability
- `INTEGRATION-BACKLOG.md` — tracks tasks that don't map onto the project directly
- `modules/_workflow/git-workflow.md` — the branch/commit/PR convention used from module 00.5 on
- `modules/<NN-name>/README.md` — module goal, prerequisite, and "done when" criteria
- `modules/<NN-name>/tasks/<NNN-name>.md` — individual task specs (concept, step 1, step 2,
  optional stretch goal)

See `ROADMAP.md` for the current module order — it changes as the course is redesigned, so treat
it as authoritative over any summary here.
