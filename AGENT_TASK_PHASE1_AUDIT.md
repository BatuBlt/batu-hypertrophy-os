# Agent Task — Phase 1 Architecture Audit

## Objective
Audit the existing application before implementing new personalization features.

## Scope
Inspect the complete current codebase and document:
- authentication and registration flow
- onboarding flow and validation
- duplicate forms, IDs, validators, and event listeners
- Supabase client usage and database assumptions
- profile persistence and RLS assumptions
- TR / EN / PL translation architecture and hard-coded UI strings
- workout data/model architecture
- progression / overload recording architecture
- service worker and cache behavior
- mobile/desktop responsive structure
- hard-coded personal/user-specific values
- legacy or duplicated code
- current testing/CI setup

## Known blocker
The onboarding has repeatedly produced `Fill in the required fields.` even when fields appear filled. Find the root cause. Do not patch the message blindly.

## Rules
- Do not add product features during the audit.
- Do not delete working functionality.
- Do not change production behavior unless required to safely inspect/fix the blocker.
- Prefer one canonical implementation over duplicated systems.
- Record evidence: file paths, relevant functions/selectors, and concrete failure points.

## Deliverable
Produce `PHASE1_AUDIT.md` containing:
1. Current architecture map
2. Current data/auth flow
3. Translation architecture
4. Onboarding validation flow
5. Root cause(s) of the current blocker
6. Duplicate/legacy code list
7. Security/RLS risks
8. Mobile/UI risks
9. Recommended target architecture
10. Ordered implementation plan for Phase 1
11. Tests required before Phase 1 can be marked complete

Do not mark Phase 1 complete from this task. This task is audit-only.
