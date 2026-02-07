# Story s001: Stock Level Tracking

**Epic:** [v012-inventory](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 4 hours

## User Story
As a clinic manager, I want real-time stock levels so I never run out of supplies.

## Acceptance Criteria
- [ ] Real-time stock count display
- [ ] Stock movement history
- [ ] Batch/lot tracking
- [ ] Location tracking (multiple storage areas)
- [ ] Barcode scanning support

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create stock_movements table | 30m | ⬜ | — |
| T002 | Build stock dashboard UI | 1h | ⬜ | — |
| T003 | Implement movement history log | 45m | ⬜ | — |
| T004 | Add batch/lot number tracking | 45m | ⬜ | — |
| T005 | Create location management | 30m | ⬜ | — |
| T006 | Integrate barcode scanner | 30m | ⬜ | — |

## Technical Notes
- Use triggers for auto stock updates
- Barcode: use quagga2 library
