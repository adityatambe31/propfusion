# US1-T1 - Set up Next.js Project & Folder Structure

- Labels: Setup, Sprint 1
- Milestone: Sprint 1 - Authentication & Portfolio Setup
- Assignee: Aditya Tambe
- Story Points: 3
- Priority: Must
- FR Reference: FR-AUTH-01

## User Story / Task Description
As a developer, I want to set up the Next.js project with a clean folder structure so that the team has a consistent codebase foundation to build upon.

## Description
Initialize the Next.js project with TypeScript, configure ESLint and Prettier, establish the folder structure (pages, components, lib, hooks, styles, api), and push to GitHub. This sets the foundation for all Sprint 1 development.

## Acceptance Criteria
- Next.js project is initialized with TypeScript support.
- Folder structure follows agreed convention: /pages, /components, /lib, /hooks, /styles, /api.
- ESLint and Prettier are configured and enforced.
- Environment variable handling is set up (.env.local template committed).
- Project builds successfully with no TypeScript or lint errors.
- Repository is pushed to GitHub with a clear README and initial commit.

## Testing Scenarios
- Successful Build: Run npm run build and confirm 0 errors.
- Lint Check: Run npm run lint and confirm no lint errors.
- Folder Structure Verified: Clone repo and confirm all folders match the agreed structure.

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
- app/
- components/
- lib/
- hooks/
- styles/
- api/
- README.md
- .env.local template
