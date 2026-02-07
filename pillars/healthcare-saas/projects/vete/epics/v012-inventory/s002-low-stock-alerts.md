# Story s002: Low Stock Alerts

**Epic:** [v012-inventory](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 3 hours

## User Story
As a clinic manager, I want automatic alerts when stock is low so I can reorder in time.

## Acceptance Criteria
- [ ] Configurable minimum stock levels per product
- [ ] Email alerts when below threshold
- [ ] In-app notifications
- [ ] Daily low stock summary
- [ ] Snooze/dismiss options

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Add min_stock_level to products table | 20m | ⬜ | — |
| T002 | Create stock check cron job | 45m | ⬜ | — |
| T003 | Implement email alert template | 30m | ⬜ | — |
| T004 | Build in-app notification system | 45m | ⬜ | — |
| T005 | Create daily summary email | 30m | ⬜ | — |
| T006 | Add snooze/dismiss functionality | 20m | ⬜ | — |

## Technical Notes
- Run stock check every hour
- Group alerts to avoid spam
