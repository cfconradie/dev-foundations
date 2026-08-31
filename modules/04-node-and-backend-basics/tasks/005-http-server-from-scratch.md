# Task 005 — HTTP server from scratch

**Concept:** before reaching for Express, build a server with Node's raw `http` module so you see
exactly what a framework is doing for you underneath — routing, headers, status codes are all
manual here.

**Step 1 — build it yourself, no AI:** using only `require("http").createServer()`, build a
server that responds differently based on `req.url` and `req.method` (e.g. GET `/` returns HTML,
GET `/api/products` returns JSON, anything else returns a 404), setting `Content-Type` headers
manually.

**Done when (step 1):** hitting each route in a browser or with `curl` returns the correct
status code, content type, and body, and you can explain what Express's routing would replace
here.

**Step 2 — AI review pass:** ask the AI what edge cases your manual router doesn't handle that
Express handles for you out of the box (trailing slashes, query strings, etc.).

**Stretch (optional):** parse a query string manually (`req.url` + `URLSearchParams`) without a
library.
