# US1-T2 - Implement Auth0 / JWT Login Flow

- Labels: Authentication, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Ali Hussein
- Story Points: 5
- Priority: Must
- FR Reference: FR-AUTH-01, FR-AUTH-02

## User Story / Task Description
As a registered user, I want to log in using my email and password so that I can securely access the PropFusion platform.

## Description
Implement the backend authentication flow using Auth0 or JWT. This includes setting up the authentication provider, handling token issuance and validation, protecting API routes, and linking user identity to the database. The login flow should support secure session management.

## Acceptance Criteria
- Auth0 (or JWT) is integrated and configured in the Next.js app.
- Users can log in with valid email and password credentials.
- Invalid credentials return a clear error without exposing which field is wrong.
- A JWT token is generated on successful login and stored securely (httpOnly cookie or secure storage).
- Protected API routes reject unauthenticated requests with HTTP 401.
- Token expiry is enforced and users are redirected to login on expiry.

## Testing Scenarios
- Valid Login: Enter correct email and password and confirm JWT issuance and dashboard redirect.
- Invalid Credentials: Enter wrong password and confirm error without token issuance.
- Expired Token: Wait for expiry and confirm redirect to login.
- Unauthenticated API Call: Call protected endpoint without token and confirm HTTP 401.

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
- lib/auth/auth.ts
- app/api/auth/[...all]/route.ts
- proxy.ts
- lib/auth/auth-client.ts
