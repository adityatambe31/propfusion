# US2-T3 - Load Domain-Specific Dashboard on Portfolio Selection

- Labels: Frontend, Portfolio, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Aditya Tambe
- Story Points: 3
- Priority: Must
- FR Reference: FR-PORT-02

## User Story / Task Description
As a logged-in user, I want the dashboard to reflect my selected portfolio type so that I see only the modules and data relevant to my domain.

## Description
Implement conditional dashboard rendering based on the user's saved portfolio type. The Real Estate dashboard loads property-specific modules (properties, tenants, leases). The Agriculture dashboard loads land/crop-specific modules. Navigation and sidebar items should update dynamically based on the selected type.

## Acceptance Criteria
- Real Estate dashboard displays: Properties, Tenants, Leases, and Financial modules.
- Agriculture dashboard displays: Land Parcels, Crops, Equipment, and Harvest modules.
- Dashboard header and sidebar navigation items update based on portfolio type.
- Switching portfolio type reloads the correct dashboard without a full page refresh.
- Empty state is shown if no assets exist yet for the selected portfolio type.
- Dashboard loads within 2 seconds of portfolio selection.

## Testing Scenarios
- Real Estate Dashboard Loads Correctly: Select Real Estate and confirm the correct nav modules.
- Agriculture Dashboard Loads Correctly: Select Agriculture and confirm land/crop modules.
- Empty State Display: Select Agriculture with no data and confirm empty state message.
- Dashboard Load Time: Measure time from selection click to render and confirm under 2 seconds.

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
- app/dashboard/page.tsx
- app/dashboard/layout.tsx
- components/dashboard/Sidebar.tsx
- components/dashboard/MobileHeader.tsx
- components/dashboard/PortfolioCharts.tsx
- components/dashboard/SmartReportDialog.tsx
