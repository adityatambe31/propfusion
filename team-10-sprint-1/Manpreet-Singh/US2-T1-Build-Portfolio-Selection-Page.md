# US2-T1 - Build Portfolio Selection Page (Real Estate / Agriculture)

- Labels: Frontend, Portfolio, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Manpreet Singh
- Story Points: 3
- Priority: Must
- FR Reference: FR-PORT-01, FR-PORT-02

## User Story / Task Description
As a logged-in user, I want to select between a Real Estate or Agricultural portfolio type so that the platform tailors its features and dashboard to my property domain.

## Description
Build the portfolio selection page displayed immediately after login. The page presents two clear options - Real Estate and Agriculture - each as a visually distinct card with a description. Upon selection, the user's preference is saved and they are routed to the appropriate domain dashboard.

## Acceptance Criteria
- Page is displayed immediately after successful login.
- Two portfolio types are shown: Real Estate and Agriculture, each as a selectable card.
- Selecting a portfolio type navigates the user to the corresponding domain dashboard.
- Page is responsive across mobile, tablet, and desktop.
- Previously selected portfolio type is pre-highlighted if the user has logged in before.
- User can switch portfolio type from account settings without losing existing data.

## Testing Scenarios
- Real Estate Portfolio Selected: Click Real Estate and confirm routing to the Real Estate dashboard.
- Agriculture Portfolio Selected: Click Agriculture and confirm routing to the Agriculture dashboard.
- Mobile View: Load page on 375px width and confirm stacked cards.
- Returning User Pre-selection: Log in again and confirm the prior portfolio is highlighted.

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
- app/onboarding/select-portfolio/page.tsx
- components/ui/card.tsx
- components/ui/button.tsx
- app/api/users/portfolio/route.ts
