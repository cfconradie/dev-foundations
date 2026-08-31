# Roadmap

Order matters — each module leans on the one before it. Don't skip ahead even if a later module
looks more exciting; the point is depth, and depth compounds.

| # | Module | Goal | Tasks |
|---|--------|------|-------|
| 00 | `html-css-tailwind-basics` | Read/structure a page, use Tailwind utility classes competently | ~6 |
| 01 | `js-fundamentals` | The real depth work: variables → types → functions → scope → closures → async → modules | ~20 |
| 02 | `dom-and-browser` | Make JS actually touch a page: query/manipulate DOM, events, fetch, storage | ~12 |
| 03 | `typescript-foundations` | Add types to what you already know in JS: types, interfaces, generics, narrowing | ~12 |
| 04 | `node-and-backend-basics` | JS on the server: Node runtime, npm, Express, a REST endpoint, a real DB | ~12 |
| 05 | `capstone-vanilla` | Ship a real app: the pricing/quote calculator, full stack, Tailwind-styled, deployed | 1 spec |
| 06 | `vue-rebuild` | Learn Vue by rebuilding the capstone in it | ~10 + rebuild |
| 07 | `react-rebuild` | Learn React by rebuilding the capstone in it (React "transfers" from Vue) | ~10 + rebuild |

## Why this order

- **HTML/CSS first but small.** You need just enough to not be blocked, not a whole module's
  worth of depth — CSS mastery isn't the goal here, and Tailwind means you rarely hand-write CSS
  again after module 00.
- **JS fundamentals is the biggest module on purpose.** This is where "thinking developer" is
  actually built: understanding scope, closures, the event loop, async — not memorizing syntax.
  Everything after this module is really "JS concepts, wearing a different outfit."
- **TypeScript before Node**, so by the time you're writing a backend you're already typing your
  functions instead of bolting types on as an afterthought.
- **Capstone before frameworks.** You should be able to build a real, working, deployed app in
  plain JS/Node before a framework does anything for you. Otherwise you don't know which parts of
  "the app working" are the framework and which parts are you.
- **Vue before React.** Vue is closer to plain JS/HTML in how it reads, and it's already a core
  stack skill worth having on its own. React concepts (components, props, state, hooks) transfer
  cleanly from Vue once you've built the same app there first.

## Progress tracking

Log every completed task in `PROGRESS.md` — one line per task with the date and what the AI
review pass actually taught you. Don't just check boxes; the sentence is the point.
