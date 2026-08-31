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

## Structure

- `README.md` — the no-AI-first rule and how to use a task
- `ROADMAP.md` — module order and reasoning
- `PROGRESS.md` — checklist of every task; the user ticks a box and writes one line on what the
  AI review taught them once both steps are done
- `modules/<NN-name>/README.md` — module goal, prerequisite, and "done when" criteria
- `modules/<NN-name>/tasks/<NNN-name>.md` — individual task specs (concept, step 1, step 2,
  optional stretch goal)

Module order: `00-html-css-tailwind-basics → 01-js-fundamentals → 02-dom-and-browser →
03-typescript-foundations → 04-node-and-backend-basics → 05-capstone-vanilla → 06-vue-rebuild →
07-react-rebuild`. The capstone (05) is a pricing/quote calculator built in vanilla JS/Node, then
rebuilt identically in Vue (06) and React (07).
