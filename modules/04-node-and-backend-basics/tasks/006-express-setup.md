# Task 006 — Express setup

**Concept:** Express is a thin routing/middleware layer over the raw `http` server from task
005 — now that you've seen the manual version, Express's `app.get(path, handler)` should look
like exactly what it is: a nicer way to do the same thing.

**Step 1 — build it yourself, no AI:** install Express, rebuild task 005's two routes
(`/` and `/api/products`) using `app.get`, and confirm identical behavior to your manual version.

**Done when (step 1):** both versions behave the same from the outside, and you can point to the
specific lines in Express that replace your manual `req.url`/status-code logic.

**Step 2 — AI review pass:** ask the AI what `express.json()` middleware does and why you'll need
it as soon as you accept POST bodies.

**Stretch (optional):** add `app.use(express.static(...))` to serve your module 00 static page
through the same server.
