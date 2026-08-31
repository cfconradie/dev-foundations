# Module 02.5 — Data structures and algorithms

**Goal:** Big-O reasoning and the core data structures, mostly applied directly to real needs the
project actually has (efficient discount-rule lookups, catalog ordering, recursive bundle
pricing) — with a smaller, explicitly-logged track of classic generic problems for the kind of
breadth a single app can't teach, tracked in `INTEGRATION-BACKLOG.md`.

**Prerequisite:** module 02 (enough JS/DOM to have real code worth measuring) and module 01.5
(you already know how to verify a claim about your own code instead of taking it on faith).

**Done when:** you can explain the Big-O of code you wrote (not just recite definitions), and
you've applied at least one technique from this module back into the real project.

**Authoring status (pilot):** only task 003 exists right now — this module is a redesign pilot.
The full ~12-task sequence is in the course redesign plan but not yet written. Module 01 is fully
authored, so task 003 measures the real `Map`-based `findRuleById` in `project/pricing.js` against
a synthetic stress-test, rather than building disconnected throwaway code.
