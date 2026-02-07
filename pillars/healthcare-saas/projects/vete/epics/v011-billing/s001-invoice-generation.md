# Story s001: Invoice Generation

**Epic:** [v011-billing](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 5 hours

## User Story
As a receptionist, I want to generate professional invoices so clients have proper documentation.

## Acceptance Criteria
- [ ] Auto-generate invoice from consultation
- [ ] Add line items (services, products)
- [ ] Calculate taxes (IVA)
- [ ] PDF generation
- [ ] Email invoice to client
- [ ] Invoice numbering system

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create invoice data model | 30m | ⬜ | — |
| T002 | Build invoice creation form | 1h | ⬜ | — |
| T003 | Implement line items management | 45m | ⬜ | — |
| T004 | Add tax calculation logic | 30m | ⬜ | — |
| T005 | Create PDF template with jsPDF | 1h | ⬜ | — |
| T006 | Implement email sending | 45m | ⬜ | — |
| T007 | Add auto-increment invoice numbers | 30m | ⬜ | — |

## Technical Notes
- IVA: 10% in Paraguay
- Invoice format: VETE-2026-00001
- Support multiple currencies
