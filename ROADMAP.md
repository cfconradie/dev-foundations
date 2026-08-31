# Roadmap

Order matters — each module leans on the one before it. Don't skip ahead even if a later module
looks more exciting; the point is depth, and depth compounds.

**Authoring status:** this roadmap reflects the full redesigned course. Only the modules marked
`authored` in the table below actually have task files written — the rest are outlines from the
redesign plan, not yet built. See "Authoring status" below the table for what that means
practically.

| # | Module | Goal | Tasks | Status |
|---|--------|------|-------|--------|
| 00 | `html-css-tailwind-basics` | Read/structure a page, use Tailwind utility classes competently — building the project's real landing page | ~6 | pre-redesign content, retrofit pending |
| 00.5 | `project-kickoff` | Write the project spec, set up the git workflow and integration backlog | 3 | authored |
| 01 | `js-fundamentals` | The real depth work: variables → types → functions → scope → closures → async → modules, plus prototypes/`this`/classes/event loop — implementing the project's real pricing logic | ~24 | pre-redesign content, retrofit pending |
| 01.5 | `testing-fundamentals` | Automated testing as a first-class skill: assertions, Vitest, AAA pattern, edge cases, mocking — testing the project's real pricing logic | ~6 | pilot: 1 of 6 authored |
| 02 | `dom-and-browser` | Make JS actually touch a page: query/manipulate DOM, events, fetch, storage — building the project's real UI | ~14 | pre-redesign content, retrofit pending |
| 02.5 | `data-structures-and-algorithms` | Big-O reasoning, hash maps, recursion, sorting/searching — mostly applied to real project needs, with a logged generic-practice track | ~12 | pilot: 1 of 12 authored |
| 03 | `typescript-foundations` | Add types to what you already know in JS: types, interfaces, generics, narrowing, discriminated unions — typing the project's real data model | ~15 | pre-redesign content, retrofit pending |
| 04 | `node-and-backend-basics` | JS on the server: Node runtime, npm, Express, a REST endpoint, a real DB, async error handling — building the project's real backend | ~14 | pre-redesign content, retrofit pending |
| 04.5 | `security-fundamentals` | Auth, XSS, CSRF, OWASP Top 10, rate limiting — attacking and hardening the project's real endpoints | ~11 | pilot: 1 of 11 authored |
| 04.75 | `databases-and-sql` | Normalization, indexing, transactions, migrations, query performance — on the project's real schema | ~6 | not yet authored |
| 05 | `capstone-vanilla` | Assemble everything built across 00–04.75, add missing tests, deploy, structured hardening pass | 1 spec, rewritten scope | pre-redesign content, rewrite pending |
| 06 | `vue-rebuild` | Learn Vue by rebuilding the project in it, plus composition patterns, performance, a11y, component testing | ~14 | pre-redesign content, gap-fill pending |
| 07 | `react-rebuild` | Learn React by rebuilding the project in it (React "transfers" from Vue), plus the same added depth as 06 | ~14 | pre-redesign content, gap-fill pending |
| 08 | `system-design-and-architecture` | Scale the real project, ADRs, design patterns already in use, 3 generic case studies for breadth | ~13 | not yet authored |
| 09 | `networking-and-delivery` | HTTP semantics, DNS/TLS basics, CI pipeline, idempotency, deployment architecture, backlog audit | ~6 | not yet authored |

## Why this order

- **HTML/CSS first but small.** You need just enough to not be blocked, not a whole module's
  worth of depth — CSS mastery isn't the goal here, and Tailwind means you rarely hand-write CSS
  again after module 00.
- **Project kickoff (00.5) comes right after, before any real logic exists.** The project needs a
  written spec before module 01 can implement its pricing logic against something real instead of
  a throwaway example — and the git workflow needs to start before there's any real work to lose
  track of.
- **JS fundamentals is the biggest module on purpose.** This is where "thinking developer" is
  actually built: understanding scope, closures, the event loop, prototypes, `this`, async — not
  memorizing syntax. Everything after this module is really "JS concepts, wearing a different
  outfit."
- **Testing (01.5) comes immediately after JS fundamentals, not bolted on later.** You can't
  meaningfully test a UI or a backend before you can test a pure function — and by the end of
  module 01 you already have real pricing-logic functions worth testing.
- **DS&A (02.5) comes after testing but before the DOM/backend work that needs it.** Efficient
  discount-rule lookups and catalog search are real needs the project will hit in modules 02 and
  04 — this module builds the reasoning (and, where it measurably helps, the actual
  implementation) before those modules need it, with a smaller supplementary track of classic
  algorithm problems for interview-style breadth a single app can't teach.
- **TypeScript before Node**, so by the time you're writing a backend you're already typing your
  functions instead of bolting types on as an afterthought.
- **Security (04.5) and databases (04.75) sit right after backend basics, not at the end.** A
  backend without an auth/input-validation pass and a properly normalized schema isn't a finished
  backend — these two modules hard against the same project instead of being a generic add-on.
- **Capstone (05) is now an assembly-and-hardening pass, not a first build.** By the time you
  reach it, most of the app already exists from 00–04.75; the capstone's job is wiring it
  together, closing test-coverage gaps, and deploying — you should be able to point at exactly
  which lines of your own code are doing what a framework would otherwise do for you.
- **Vue before React.** Vue is closer to plain JS/HTML in how it reads, and it's already a core
  stack skill worth having on its own. React concepts (components, props, state, hooks) transfer
  cleanly from Vue once you've built the same app there first.
- **System design (08) and networking/delivery (09) come last on purpose.** You can't reason
  well about scaling, caching, or deployment architecture for a system you haven't actually built
  and shipped — these modules use the real, already-deployed project as their primary case study.

## Progress tracking

Log every completed task in `PROGRESS.md` — one line per task with the date and what the AI
review pass actually taught you. Don't just check boxes; the sentence is the point. `PROGRESS.md`
also tracks whether each task was committed on its own branch (see
`modules/_workflow/git-workflow.md`).

## Integration backlog

A few tasks (mostly in 02.5 and 08) can't map onto the project directly. `INTEGRATION-BACKLOG.md`
tracks every one of those with a planned tie-back, audited at the end of module 02.5 and again as
the final task of module 09.
