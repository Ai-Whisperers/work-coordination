# Story s001: Payment Gateway Integration

**Epic:** [v010-integrations](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 6 hours

## User Story
As a clinic, I want to accept online payments so clients can pay invoices easily.

## Acceptance Criteria
- [ ] MercadoPago integration (Paraguay focus)
- [ ] Stripe as backup option
- [ ] Payment status webhooks
- [ ] Invoice auto-update on payment
- [ ] Payment receipt emails
- [ ] Refund handling

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Set up MercadoPago SDK | 45m | ⬜ | — |
| T002 | Create payment intent API | 1h | ⬜ | — |
| T003 | Build payment UI component | 1h | ⬜ | — |
| T004 | Implement webhook handler | 1h | ⬜ | — |
| T005 | Add invoice status updates | 45m | ⬜ | — |
| T006 | Create receipt email template | 30m | ⬜ | — |
| T007 | Implement refund flow | 1h | ⬜ | — |

## Technical Notes
- MercadoPago: primary for Paraguay
- Stripe: international clients
- Store payment_id in invoices table
