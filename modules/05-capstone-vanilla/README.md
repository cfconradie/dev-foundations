# Module 05 — Capstone: Pricing/Quote Calculator

**Goal:** ship a real, deployable app using only what modules 00-04 taught you — vanilla
JS/TS, Node/Express, a real database, Tailwind. No framework. This is the checkpoint that proves
you can build something real before a framework starts doing parts of it for you.

Built the same way as every task: **design and code it yourself first, then bring in AI for an
architecture/code review pass** before calling it shipped. This one app then gets rebuilt in Vue
(module 06) and React (module 07), so build it cleanly enough to be worth rebuilding.

## Why this app

This matches the real niche already identified in the Upwork brain: **custom-JS-logic /
pricing-calculator tools**. It's realistic in scope for a solo learner, shaped like real small
Upwork jobs, and becomes an actual portfolio piece — not a todo list.

## What it does

A client-facing tool where a visitor configures a project (a set of toggles/selects representing
scope — e.g. "type of site," "number of pages," "add e-commerce," "add a CMS," "rush delivery")
and gets back an instant price estimate, with the option to submit their contact details to
request a real quote. You (the "admin") can see submitted quote requests.

## User stories

1. As a visitor, I can select project options and see the estimated price update live as I
   change them (no page reload).
2. As a visitor, I can submit my contact info + selected options as a "request a quote" form.
3. As a visitor, if I submit invalid data (missing email, etc.) I see clear inline errors.
4. As the admin, I can view a list of all submitted quote requests with their computed price and
   selected options.
5. As the admin, I can mark a quote request as "contacted" or "won"/"lost".

## Data model (design it yourself in TypeScript first, see module 03 task 012 for the pattern)

- `PricingRule` — a named option (e.g. "E-commerce") with a price delta and a category
  (base/addon), used to compute the total.
- `QuoteRequest` — the visitor's name, email, selected option ids, computed total, status
  (`"new" | "contacted" | "won" | "lost"`), and a timestamp.

## Architecture

- **Backend:** Node/Express (module 04) with a real database (SQLite or Supabase, module 04 task
  010) storing `PricingRule`s and `QuoteRequest`s, exposing a REST API: `GET /api/pricing-rules`,
  `POST /api/quote-requests`, `GET /api/quote-requests` (admin), `PATCH
  /api/quote-requests/:id` (status update).
- **Frontend:** vanilla TS + the DOM skills from module 02, styled with Tailwind (module 00) —
  live price calculation happens client-side against the fetched pricing rules; submission posts
  to the backend.
- **No framework.** This is the point — you should be able to point at exactly which lines of
  your own code are doing what a framework would otherwise do for you.

## Definition of done

- [ ] Pricing rules are stored in the database, not hardcoded in the frontend.
- [ ] Selecting/deselecting options updates the displayed price instantly, client-side.
- [ ] The quote request form validates before submitting and shows clear errors.
- [ ] Submitted quote requests are persisted and visible on a simple admin view.
- [ ] Admin can update a quote request's status and see it reflected.
- [ ] The app is deployed somewhere reachable by a real URL (e.g. Render, Railway, Fly.io, or a
  VPS you already have) — a live link is part of "done," not optional polish.
- [ ] You've done an AI architecture/code review pass on the whole thing and addressed (or
  consciously decided not to address, with a reason) its top findings.

## After shipping

Take a screenshot and write 2-3 sentences in `PROGRESS.md` about what was hardest to build and
why — this becomes real portfolio material, and the "why" is exactly the kind of thing that
distinguishes a thinking developer from someone who shipped an AI's output.
