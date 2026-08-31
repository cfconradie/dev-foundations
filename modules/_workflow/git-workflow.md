# Git workflow

Every task from module 00.5 onward uses this. It's a skill the course is building on purpose, not
paperwork — a solo learner who never branches or writes a real commit message won't have that
muscle when it actually matters.

## Per task

1. Branch off `main`: `git checkout -b task/<module>-<NNN>-<slug>` (e.g.
   `task/01.5-003-aaa-pattern-testing-pricing-logic`).
2. Do the task's Step 1 on that branch. Commit as you go — at minimum one commit when Step 1 is
   done, with a message that says *what* changed and, in the body if it's not obvious, *why*. Not
   `wip` or `done`.
3. Do Step 2 (the AI review) on the same branch. If you act on a finding, that's another commit.
4. Before merging, write a one-paragraph PR description for yourself: what this task added, and
   what you'd flag if someone else were reviewing it. This is the closest thing in the course to
   reviewing someone else's diff — read your own like you didn't write it.
5. Merge to `main` (a real `git merge` or `gh pr create && gh pr merge` if you want the practice
   with GitHub's flow — either is fine, the habit is what matters).

## Why this exists

- A task branch means you can look back at exactly what one 15-minute session produced, which is
  useful when a later module asks you to revisit something.
- A real commit message is a forcing function: if you can't describe what you did in one line,
  you probably don't understand it as well as you think.
- The self-authored PR description is deliberate practice at the skill AI-review can't give you —
  reading a diff critically, cold, the way a teammate would.

## What "Done when" means from here on

Every task file's done-when criteria includes, implicitly, "committed on its task branch with a
descriptive message" — this file is what that bullet refers to, so individual tasks don't have to
repeat it.
