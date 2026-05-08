# US1-T3 - Build Login UI Page

- Labels: Frontend, Authentication, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Aditya Tambe
- Story Points: 3
- Priority: Must
- FR Reference: FR-AUTH-02

## User Story / Task Description
As a registered user, I want to see a clean, responsive login page where I can enter my email and password to access the system.

## Description
Design and implement the Login UI page using Next.js and Tailwind CSS. The page should include an email field, password field, submit button, error display, and a link to the password reset flow. It must be fully responsive and match the PropFusion design system.

## Acceptance Criteria
- Login page is accessible at /login without authentication.
- Form contains email input, password input (masked), and a submit button.
- Form validates required fields client-side before submission.
- Error messages display clearly below the form on failed login.
- Successful login redirects user to the portfolio selection page.
- Page is responsive across mobile, tablet, and desktop breakpoints.
- A Forgot Password? link is visible and navigates to the reset flow.

## Testing Scenarios
- Successful Login Redirect: Submit valid credentials and confirm redirection to portfolio selection.
- Empty Field Validation: Submit with empty email and confirm client-side validation.
- Failed Login Error Display: Submit invalid credentials and confirm inline error without page reload.
- Mobile Responsiveness: Load /login at 375px and confirm no overflow.

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
- app/auth/sign-in/page.tsx
- components/auth/AuthLayout.tsx
- components/ui/input.tsx
- components/ui/button.tsx
- components/ui/label.tsx
- app/globals.css
