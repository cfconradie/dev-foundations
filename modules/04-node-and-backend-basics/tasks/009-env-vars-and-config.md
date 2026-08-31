# Task 009 — Env vars and config

**Concept:** hardcoding secrets/ports/URLs in source code is a real security and deployment
problem — environment variables (via `.env` + `dotenv`) let you configure the same code
differently per environment (local/staging/prod) without changing it.

**Step 1 — build it yourself, no AI:** move your server's port and a fake `API_KEY` into a `.env`
file, load it with `dotenv`, use `process.env.PORT`/`process.env.API_KEY` in code, and add `.env`
to `.gitignore` (create a `.env.example` with placeholder values instead).

**Done when (step 1):** changing `.env` changes the running port without touching code, and
`.env` itself is confirmed excluded from `git status`.

**Step 2 — AI review pass:** ask the AI what real-world incident class this pattern prevents
(hint: secrets committed to a public GitHub repo) and how to check if you've ever done that in a
past project (`git log -p | grep`-style history search).

**Stretch (optional):** add a startup check that exits with a clear error if a required env var
is missing.
