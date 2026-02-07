# Story s001: Lab Test Ordering

**Epic:** [v020-laboratory](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 5 hours

## User Story
As a veterinarian, I want to order lab tests from the consultation so the process is streamlined.

## Acceptance Criteria
- [ ] Test catalog with categories
- [ ] Order from consultation screen
- [ ] Sample collection tracking
- [ ] Priority levels (routine/urgent/stat)
- [ ] Print lab requisition
- [ ] Track order status

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create lab_tests catalog table | 30m | ⬜ | — |
| T002 | Build test order form | 1h | ⬜ | — |
| T003 | Create lab_orders table | 30m | ⬜ | — |
| T004 | Implement sample tracking | 45m | ⬜ | — |
| T005 | Add priority selection | 20m | ⬜ | — |
| T006 | Create lab requisition PDF | 45m | ⬜ | — |
| T007 | Build order status workflow | 45m | ⬜ | — |
| T008 | Add notifications on status change | 25m | ⬜ | — |

## Technical Notes
- Status: ordered → collected → processing → complete
- Integration with external labs later
