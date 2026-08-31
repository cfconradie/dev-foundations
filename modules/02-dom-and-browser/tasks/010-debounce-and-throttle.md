# Task 010 — Debounce and throttle

**Concept:** an input or scroll event can fire dozens of times per second — debounce (wait for a
pause) and throttle (limit to once per interval) are closures (module 01, task 011) applied to
solve a real performance problem, so this task ties two earlier concepts together.

**Step 1 — build it yourself, no AI:** write your own `debounce(fn, delay)` from scratch (using
`setTimeout` + closure, not a library), attach it to a search input's `keyup` event so a
(fake) search function only fires 300ms after the user stops typing, and log every keystroke vs
every actual search call to see the difference.

**Done when (step 1):** typing quickly logs many keystrokes but only one search call, fired after
you stop typing.

**Step 2 — AI review pass:** ask the AI to explain, using your own debounce code, exactly why the
timer resets on every keystroke — make sure you can trace it in the closure, not just take the
explanation on faith.

**Stretch (optional):** implement `throttle(fn, interval)` too and explain a scenario where
throttle is the better fit than debounce (e.g. scroll position tracking).
