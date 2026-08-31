# Task 002 — Init the git workflow

**Concept:** a commit message you can't write clearly is a sign you don't understand what you
just did as clearly as you think — branching per task also means you can look back at exactly
what one session produced, which matters later when a review-checkpoint task asks you to revisit
something.

**Where this goes:** project-track — this is you establishing the workflow every task from here
on actually uses, not a one-off exercise.

**Step 1 — build it yourself, no AI:** read `modules/_workflow/git-workflow.md` in full first —
this task is you actually using it, not reading about it. Create a task branch for *this* task
(`task/00.5-002-init-the-git-workflow`), make at least one real commit on it as you do the rest of
this task, then write a one-paragraph PR description for yourself: what this task added, and one
thing you'd flag if someone else were reviewing your commit history so far.

**Done when (step 1):** you have one commit on a correctly-named task branch, and a written PR
description in your own words (paste it into this task's line in `PROGRESS.md` or keep it in the
merge commit body — your choice, but it has to exist somewhere you can find it again).

**Step 2 — AI review pass:** paste your commit message(s) so far and ask: "If you only had these
commit messages and no other context, what would you be unable to tell about what I actually
built or why? Be specific about what's missing, not just 'add more detail.'" Note the answer in
`PROGRESS.md`.

**Stretch (optional):** use `gh pr create` against a throwaway branch to practice the real GitHub
flow instead of a local-only merge.
