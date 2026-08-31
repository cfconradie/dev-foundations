# Task 001 — Semantic HTML skeleton

**Concept:** HTML tags describe *meaning*, not appearance (`<nav>`, `<main>`, `<article>` vs a
pile of `<div>`s) — this is what screen readers, SEO, and other developers rely on to understand
your page without reading your CSS.

**Step 1 — build it yourself, no AI:** Create `index.html` for a one-page site (e.g. "My Dev
Log") using only semantic tags: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
No `<div>` allowed except where no semantic tag fits.

**Done when (step 1):** the page opens in a browser, and every top-level section uses a semantic
tag you can justify out loud ("this is `<nav>` because...").

**Step 2 — AI review pass:** paste your HTML and ask: "Which of these tags did I choose wrong or
could improve, and why does semantic HTML matter beyond styling?" Note the answer in PROGRESS.md.

**Stretch (optional):** add ARIA landmarks and check the page with a screen reader (VoiceOver on
Mac, Cmd+F5).
