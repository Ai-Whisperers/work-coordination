# Story s003: Patient Visit Analytics

**Epic:** [v007-analytics](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 4 hours

## User Story
As a clinic manager, I want to see patient visit patterns so I can optimize scheduling.

## Acceptance Criteria
- [ ] Visits per day/week/month
- [ ] Peak hours heatmap
- [ ] New vs returning patients
- [ ] No-show rate tracking
- [ ] Average visit duration

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create visits aggregation API | 1h | ⬜ | — |
| T002 | Build visits trend chart | 45m | ⬜ | — |
| T003 | Implement peak hours heatmap | 1h | ⬜ | — |
| T004 | Add patient segmentation (new/returning) | 45m | ⬜ | — |
| T005 | Track and display no-show rates | 30m | ⬜ | — |

## Technical Notes
- Use appointments + consultations tables
- Heatmap: 7 days x 24 hours grid
