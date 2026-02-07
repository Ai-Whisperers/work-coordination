# Story s001: Email Notifications

**Epic:** [v017-notifications](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 4 hours

## User Story
As a pet owner, I want email reminders so I don't forget appointments and vaccinations.

## Acceptance Criteria
- [ ] Appointment reminder (24h before)
- [ ] Vaccination due reminders
- [ ] Invoice/receipt emails
- [ ] Customizable templates
- [ ] Unsubscribe option

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Set up email service (Resend/SendGrid) | 30m | ⬜ | — |
| T002 | Create email template system | 45m | ⬜ | — |
| T003 | Build appointment reminder job | 45m | ⬜ | — |
| T004 | Create vaccination reminder job | 45m | ⬜ | — |
| T005 | Implement invoice email | 30m | ⬜ | — |
| T006 | Add template editor for clinics | 30m | ⬜ | — |
| T007 | Implement unsubscribe handling | 25m | ⬜ | — |

## Technical Notes
- Use Resend for transactional email
- React Email for templates
