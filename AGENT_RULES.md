# Hypertrophy OS — Agent Rules

## Mission
Develop Hypertrophy OS into a production-quality, personalized fitness platform. Work phase-by-phase, preserve working functionality, and fix root causes instead of stacking patches.

## Non-negotiable rules
- Inspect the existing architecture before changing code.
- Never create duplicate authentication, onboarding, validation, translation, profile, or database systems.
- Do not remove working functionality unless explicitly required.
- Every user-facing string must support TR / EN / PL.
- Personal data must come from the authenticated user's profile/database; never hard-code one user's values.
- Respect Supabase RLS and never expose secret/service-role keys in frontend code.
- Mobile and desktop are both first-class targets.
- After meaningful changes, run syntax/lint/tests and regression checks.
- If a bug appears, identify the root cause before patching it.
- Refactor when the existing structure is causing repeated bugs; do not keep layering workarounds.
- Do not mark a phase complete until its acceptance criteria are tested.

## Current blocker
The onboarding has repeatedly shown `Fill in the required fields.` despite visible fields being filled. Treat this as a root-cause architecture problem. Audit for duplicate IDs, duplicate forms, duplicate validators, stale/legacy code, event-handler conflicts, and language-state conflicts before adding new onboarding features.

## Development workflow
1. Audit.
2. Write a short implementation plan.
3. Implement in a focused change.
4. Test.
5. Fix failures.
6. Regression-check existing features.
7. Report files changed, tests, remaining risks, and next step.

## Product roadmap
See `PROJECT_ROADMAP.md`. Complete phases in order.
