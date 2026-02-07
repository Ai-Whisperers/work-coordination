# Story s001: GitHub Actions Templates

**Epic:** [a001-ci-cd](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 4 hours

## User Story
As a developer, I want reusable CI/CD templates so all repos have consistent pipelines.

## Acceptance Criteria
- [ ] Node.js test workflow
- [ ] Python test workflow
- [ ] Build and deploy workflow
- [ ] PR validation checks
- [ ] Semantic release workflow
- [ ] Dependency update workflow

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create node-test.yml template | 30m | ⬜ | — |
| T002 | Create python-test.yml template | 30m | ⬜ | — |
| T003 | Create deploy.yml with environments | 45m | ⬜ | — |
| T004 | Create pr-checks.yml | 30m | ⬜ | — |
| T005 | Add semantic-release.yml | 30m | ⬜ | — |
| T006 | Create renovate config | 30m | ⬜ | — |
| T007 | Document usage in README | 30m | ⬜ | — |
| T008 | Create .github repo for org | 15m | ⬜ | — |

## Technical Notes
- Store in Ai-Whisperers/.github
- Use composite actions for reuse
