# Task 005 — Tailwind responsive and state variants

**Concept:** Tailwind's `md:`, `hover:`, `focus:` prefixes are conditional versions of the same
utility classes — this is the pattern behind almost all "advanced" Tailwind you'll see later.

**Step 1 — build it yourself, no AI:** take your card row and make it: single column on mobile,
3 columns on `md:` and above; each card gets a `hover:` shadow and `focus:` ring on its button.

**Done when (step 1):** resizing the browser window changes the layout at the breakpoint, and
hover/focus states are visibly different from the resting state.

**Step 2 — AI review pass:** ask the AI which responsive breakpoint choice (`sm`/`md`/`lg`) is
most conventional for a 3-card layout and why.

**Stretch (optional):** add a `dark:` variant for a dark-mode version of the cards.
