# Story s001: Multi-Vet Calendar

**Epic:** [v013-scheduling](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 6 hours

## User Story
As a receptionist, I want to see all vets' schedules in one view so I can book appointments efficiently.

## Acceptance Criteria
- [ ] Side-by-side vet calendars
- [ ] Drag-and-drop appointment moving
- [ ] Color coding by appointment type
- [ ] Vet availability indicators
- [ ] Filter by vet/service type
- [ ] Week/day/month views

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Integrate FullCalendar library | 45m | ⬜ | — |
| T002 | Create multi-resource view | 1h | ⬜ | — |
| T003 | Implement drag-and-drop | 1h | ⬜ | — |
| T004 | Add color coding system | 30m | ⬜ | — |
| T005 | Build availability overlay | 45m | ⬜ | — |
| T006 | Create filter sidebar | 45m | ⬜ | — |
| T007 | Implement view switching | 30m | ⬜ | — |
| T008 | Add real-time updates | 45m | ⬜ | — |

## Technical Notes
- Use @fullcalendar/react
- Real-time via Supabase subscriptions
