# US1-T4 - Implement Role-Based Access Control (RBAC) Middleware

- Labels: Authentication, Backend, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Ali Hussein
- Story Points: 5
- Priority: Must
- FR Reference: FR-AUTH-03

## User Story / Task Description
As an administrator, I want to assign roles to users so that each user only accesses features relevant to their responsibilities.

## Description
Implement RBAC middleware that reads the user's role from the JWT token and enforces route-level and API-level access restrictions. Four roles are supported: Owner, Manager, Financial Stakeholder, and Administrator. Middleware must block unauthorized access and return appropriate HTTP responses.

## Acceptance Criteria
- Four roles are defined in the system: Owner, Manager, Financial Stakeholder, Administrator.
- User role is embedded in the JWT token at login.
- Middleware validates the role on every protected API route request.
- Accessing a restricted route without the correct role returns HTTP 403.
- Administrators can view and update user roles via an admin API endpoint.
- Role restrictions are enforced server-side, not only client-side.

## Testing Scenarios
- Owner Accesses All Features: Log in as Owner and confirm full dashboard access.
- Manager Blocked from Financial Admin: Log in as Manager and confirm HTTP 403 on restricted endpoint.
- Unauthorized Route Blocked: Attempt /admin without Administrator role and confirm redirect or block.
- Admin Assigns Role: PUT /api/users/:id/role and confirm role update.

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
- proxy.ts
- app/api/users/:id/role/route.ts
- app/api/admin/financials/route.ts
- lib/auth/auth.ts
