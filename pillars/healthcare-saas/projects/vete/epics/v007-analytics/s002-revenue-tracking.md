# Story s002: Revenue Tracking

**Epic:** [v007-analytics](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 5 hours

## User Story
As a clinic owner, I want to track revenue over time so I can monitor business health.

## Acceptance Criteria
- [ ] Daily/weekly/monthly revenue charts
- [ ] Revenue by service type breakdown
- [ ] Comparison with previous period
- [ ] Revenue goals and progress
- [ ] Export data to CSV

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create revenue aggregation API endpoint | 1h | ⬜ | — |
| T002 | Build RevenueChart component | 1h | ⬜ | — |
| T003 | Implement service breakdown pie chart | 45m | ⬜ | — |
| T004 | Add period comparison logic | 1h | ⬜ | — |
| T005 | Create revenue goals UI | 45m | ⬜ | — |
| T006 | Implement CSV export | 30m | ⬜ | — |

## Technical Notes
- Aggregate from invoices table
- Cache results for performance
- Real-time updates via subscription
