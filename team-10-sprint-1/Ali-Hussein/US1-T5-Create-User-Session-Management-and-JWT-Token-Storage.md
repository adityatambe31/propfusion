# US1-T5 - Create User Session Management & JWT Token Storage

- Labels: Authentication, Backend, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Ali Hussein
- Story Points: 3
- Priority: Must
- FR Reference: FR-AUTH-02

## User Story / Task Description
As a logged-in user, I want my session to remain active while I work and to be securely terminated when I log out.

## Description
Implement secure session management including JWT token storage strategy (httpOnly cookies), token refresh logic, and a logout endpoint that invalidates the session. Ensure tokens are not accessible via JavaScript to prevent XSS attacks.

## Acceptance Criteria
- JWT is stored in an httpOnly cookie (not localStorage) after login.
- Session persists across page refreshes without requiring re-login.
- Token expiry is enforced; expired sessions redirect to login.
- A POST /api/auth/logout endpoint clears the cookie and invalidates the session.
- Logout from one tab invalidates the session across all tabs.
- Token is not accessible via document.cookie or JavaScript.

## Testing Scenarios
- Session Persistence: Log in, refresh the page, and confirm the session remains active.
- Logout Clears Session: Log out and confirm protected routes redirect to login.
- Token Not Accessible via JS: Open browser console and confirm JWT cookie is not visible.
- Expired Token Redirect: Simulate expiry and confirm redirect to /login.

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
- app/api/auth/logout/route.ts
- lib/auth/auth.ts
- app/api/auth/[...all]/route.ts
- proxy.ts
