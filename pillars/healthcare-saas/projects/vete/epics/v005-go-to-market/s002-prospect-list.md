# S002: Prospect List

**Epic:** [v005-go-to-market](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~2 hours

---

## User Story

**As a** founder  
**I want** a list of potential clinic customers  
**So that** I can systematically reach out to them

---

## Acceptance Criteria

- [ ] 20+ vet clinics in Asunción/Gran Asunción
- [ ] Contact info (phone, WhatsApp, email)
- [ ] Decision maker name if available
- [ ] Clinic size estimate (small/medium/large)
- [ ] Tracked in spreadsheet or CRM

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Search Google Maps for vet clinics | 30m | ✅ | Nyx 🌙 |
| T002 | Search Instagram/Facebook for clinics | 30m | ⬜ | — |
| T003 | Get contact info from websites | 30m | ⏳ | Nyx 🌙 |
| T004 | Create tracking spreadsheet | 15m | ✅ | Nyx 🌙 |
| T005 | Prioritize by size/potential | 15m | ✅ | Nyx 🌙 |

---

## Target Areas

### Asunción
- Villa Morra
- Carmelitas
- Centro
- Recoleta
- Mburucuyá

### Gran Asunción
- San Lorenzo
- Luque
- Fernando de la Mora
- Lambaré

---

## Spreadsheet Columns

| Column | Description |
|--------|-------------|
| Clinic Name | Business name |
| Location | Neighborhood/city |
| Size | Small (<3 vets), Medium (3-6), Large (7+) |
| Contact Name | Owner/manager name |
| Phone | WhatsApp number |
| Email | If available |
| Instagram | Handle |
| Status | Not contacted, Contacted, Demo scheduled, etc. |
| Notes | Any relevant info |
| Priority | High/Medium/Low |

---

## Technical Notes

### T004 Complete (2026-02-06 - Nyx 🌙)

Created tracking system at `/home/ai-whisperers/Vete/sales/`:
- `prospects.csv` — Initial list with 9 clinics from target areas
- `README.md` — Status values, priority definitions, usage guide

CSV columns: Clinic Name, Location, Size, Contact Name, Phone, Email, Instagram, Website, Status, Priority, Notes, Last Contact, Next Action

Committed to Vete repo: `feat(sales): add prospect tracking spreadsheet and README`

### T005 Complete (2026-02-07 - Nyx 🌙)

Added scoring system (0-100) based on:
- Size (+10/20/30)
- Premium location (+20)
- Website/Instagram (+15/10)
- Proximity to San Lorenzo (+15)
- Warm intro (+25)

**Top 4 Priorities:**
1. Hospital Veterinario Acosta Ñu (95)
2. Clínica Veterinaria del Sol (90)
3. Veterinaria San Roque (88)
4. Pet Center Paraguay (85)
