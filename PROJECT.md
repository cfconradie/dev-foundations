# Project: Pricing/Quote Calculator

This is the one running project the whole course builds, starting at module 00.5. It's not a
capstone bolted on at the end — every module from here on either adds a real piece of this app or
is explicitly logged in `INTEGRATION-BACKLOG.md` as a detour with a planned tie-back.

This file is the single source of truth for the spec. It grows as modules add capability — each
change gets a dated line in the changelog at the bottom so you (and any later module) can see
exactly what existed when.

## What it does

A client-facing tool where a visitor configures a project (a set of toggles/selects representing
scope — e.g. "type of site," "number of pages," "add e-commerce," "add a CMS," "rush delivery")
and gets back an instant price estimate, with the option to submit their contact details to
request a real quote. The admin can see submitted quote requests and update their status.

This matches a real niche: custom-JS-logic / pricing-calculator tools are a common small-scope
freelance job. It's realistic for a solo learner, shaped like a real job, and becomes an actual
portfolio piece — not a todo list.

## User stories

1. As a visitor, I can select project options and see the estimated price update live as I
   change them (no page reload).
2. As a visitor, I can submit my contact info + selected options as a "request a quote" form.
3. As a visitor, if I submit invalid data (missing email, etc.) I see clear inline errors.
4. As the admin, I can view a list of all submitted quote requests with their computed price and
   selected options.
5. As the admin, I can mark a quote request as "contacted" or "won"/"lost".

## Data model

- `PricingRule` — a named option (e.g. "E-commerce") with a price delta and a category
  (base/addon), used to compute the total.
- `QuoteRequest` — the visitor's name, email, selected option ids, computed total, status
  (`"new" | "contacted" | "won" | "lost"`), and a timestamp.

These are seeds, not final — module 01 gives them real shape as JS objects/functions, module 03
gives them real TypeScript types, module 04.75 gives them a real normalized schema. Each of those
modules updates this section and logs the change below.

## Architecture (target — built incrementally, not all present yet)

- **Backend:** Node/Express with a real database, storing `PricingRule`s and `QuoteRequest`s,
  exposing a REST API: `GET /api/pricing-rules`, `POST /api/quote-requests`,
  `GET /api/quote-requests` (admin), `PATCH /api/quote-requests/:id` (status update).
- **Frontend:** vanilla TS + DOM, styled with Tailwind — live price calculation happens
  client-side against the fetched pricing rules; submission posts to the backend.
- **No framework** for the vanilla build (module 05). Rebuilt in Vue (06) and React (07) once
  the vanilla version ships, so each framework is learned by solving the same real problem again.

## Status

Nothing is built yet — this file exists so every module from 00.5 onward has a real spec to build
against instead of a disposable example. Each module updates the relevant section above when it
adds real capability, and adds one line to the changelog below.

## Changelog

- Seeded from the original module 05 capstone spec as the starting point for the whole-course
  redesign; no code exists yet.
