# Plan — CampusEats

## Process choice

### How stable and binding are the requirements?

The original request is brief and leaves many details unclear, so the requirements are likely to change after students and food vendors see early versions.

### How quickly can real feedback arrive?

Students, food vendors, and food-court staff can test a small working part and provide feedback within a few days.

### What does failure cost?

A failure could delay orders or inconvenience students, while privacy or payment mistakes could be more serious, so each small release must be tested carefully.

### How many pieces must move together?

Student ordering, vendor menus, order status, and pickup times must work together, but they can be built and checked in small connected parts.

Verdict: Use short increments because feedback can arrive quickly and the unclear requirements are likely to change.

## Milestones

| Milestone | When | What is true then |
|---|---|---|
| Menu prototype | 4 September 2026 | A tester can view at least three vendors and their available menu items. |
| Ordering test | 11 September 2026 | Five students can place an order and select a pickup time successfully. |
| Sprint review | 18 September 2026 | All Sprint 1 items meet every condition in the Definition of Done. |

## Risks

| Risk | Likelihood | Mitigation |
|---|---|---|
| Vendors do not keep menu availability accurate. | High | Give vendors a simple update checklist and check menus twice each day. |
| Lunchtime order volume makes confirmations slow. | Medium | Test the expected lunchtime order volume before the sprint review. |
| Students find the ordering steps confusing. | Medium | Test with five students early and simplify any step they cannot complete. |
