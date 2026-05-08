# US2-T2 - Store Portfolio Preference in User Profile (DB)

- Labels: Backend, Database, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Ali Hussein
- Story Points: 2
- Priority: Must
- FR Reference: FR-PORT-01

## User Story / Task Description
As a user, I want my portfolio type preference to be saved so that the system remembers my choice on future logins.

## Description
Implement the backend logic and database schema to persist the user's portfolio type selection (Real Estate or Agriculture) in the user profile table. Expose a PATCH /api/users/portfolio endpoint that updates the preference and returns the updated profile.

## Acceptance Criteria
- User profile table includes a portfolioType field (enum: real_estate, agriculture).
- PATCH /api/users/portfolio endpoint accepts and validates the portfolio type.
- Portfolio preference is saved on first selection and updated on change.
- API returns HTTP 200 with the updated user profile on success.
- Switching portfolio type does not delete previously entered asset or tenant data.
- Portfolio preference is included in the JWT payload or returned via a /api/users/me endpoint.

## Testing Scenarios
- Save Portfolio Preference: Select Agriculture and call PATCH /api/users/portfolio and confirm DB update.
- Invalid Portfolio Type Rejected: Send invalid portfolioType and confirm HTTP 400.
- Switch Portfolio Preserves Data: Switch from Real Estate to Agriculture and confirm real estate assets remain.

## Definition of Done
- Code fully implemented.
- Acceptance criteria met.
- Feature tested and working.
- No regressions introduced.
- Code merged cleanly into main branch.
- No unresolved merge conflicts.
- Documentation/comments updated if needed.
- Team agrees work is releasable.

## Files to Push
- app/api/users/portfolio/route.ts
- app/api/users/me/route.ts
- lib/db/*
- lib/types.ts
