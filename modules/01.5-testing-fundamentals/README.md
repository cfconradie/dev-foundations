# Module 01.5 — Testing fundamentals

**Goal:** automated testing as a first-class skill, not an afterthought. You can't meaningfully
test a UI or a backend before you can test a pure function — this module starts with the
pricing-logic functions the project needs, testing them the way you'll test everything else from
here on.

**Prerequisite:** module 01 (functions, pure vs. impure, module 00.5's project spec).

**Done when:** you can write a clean AAA-structured test for a pure function, explain what "edge
case" means in terms of your own code (not the textbook definition), and have a passing test
suite for the project's pricing logic.

**Authoring status (pilot):** only task 003 exists right now — this module is a redesign pilot.
The full 6-task sequence (why test, Vitest setup, AAA pattern, edge cases, mocking, mini-project)
is in the course redesign plan but not yet written. Module 01 is now fully authored, so task 003
tests the real `project/pricing.js` (built in module 01, task 028) rather than a throwaway
function — do module 01 first if you haven't.
