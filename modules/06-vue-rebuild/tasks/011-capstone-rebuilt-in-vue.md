# Task 011 — Capstone rebuilt in Vue (module capstone)

**Concept:** put it all together — the same app from module 05, now built the Vue way end to
end, backed by the same Express/database API (no need to rebuild the backend).

**Step 1 — build it yourself, no AI:** rebuild the full capstone frontend in Vue: the calculator
with live pricing (computed), the quote form (v-model + validation), routing between calculator
and admin, and the admin quote list with status updates — reusing your existing backend API
unchanged.

**Done when (step 1):** every item in module 05's Definition of Done still holds, now
Vue-powered, and you can point to which vanilla-JS module 02 code Vue eliminated entirely.

**Step 2 — AI review pass:** paste the Vue app's structure and ask for a review: is state
organized sensibly (props vs store), is anything doing DOM manipulation directly instead of the
Vue way (a smell that you're fighting the framework), is component splitting sensible. Log the
best finding.

**Stretch (optional):** add a small animation/transition (`<Transition>`) to the price update.
