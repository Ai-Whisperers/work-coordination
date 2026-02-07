# Story s002: CI Setup

**Epic:** [r001-3adic-infrastructure](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 2 hours

## User Story
As a developer, I want automated testing so PRs are validated automatically.

## Acceptance Criteria
- [ ] GitHub Actions workflow
- [ ] Run tests on push/PR
- [ ] Python version matrix (3.10, 3.11, 3.12)
- [ ] Test results in PR checks

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create .github/workflows/test.yml | 30m | ✅ | Erebus 🔥 |
| T002 | Add pytest configuration | 20m | ⏳ | Erebus 🔥 |
| T003 | Create sample tests | 30m | ⬜ | — |
| T004 | Test workflow runs | 20m | ⬜ | — |
| T005 | Add badge to README | 10m | ⬜ | — |

## Technical Notes
- Use pytest
- Cache pip dependencies
- Fail fast on first error
