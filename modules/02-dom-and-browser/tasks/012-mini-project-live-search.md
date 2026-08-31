# Task 012 — Mini project: live search (module capstone)

**Concept:** combine everything from this module — selecting/creating elements, events,
delegation, fetch, debounce — into one real feature. This is the "can you build an actual UI
interaction" checkpoint before TypeScript.

**Step 1 — build it yourself, no AI:** build a live-search box against a public API (e.g.
`jsonplaceholder.typicode.com/users` filtered client-side, or a real search API if you want a
harder version) that: debounces input, shows a loading state, renders results into a list using
event delegation for click-to-select, handles the empty-results and error cases distinctly, and
persists the last search term to localStorage so it's pre-filled on reload.

**Done when (step 1):** typing shows debounced, correctly-loading, correctly-erroring results,
selecting a result does something visible (e.g. shows its details), and the search term survives
a page reload.

**Step 2 — AI review pass:** paste the full script and ask for an architecture + bug review:
race conditions (what if an old fetch resolves after a newer one?), memory leaks (event listeners
never cleaned up), and readability. Log the single most valuable finding.

**Stretch (optional):** fix a race condition if the AI review found one (e.g. by tracking and
ignoring stale requests).
