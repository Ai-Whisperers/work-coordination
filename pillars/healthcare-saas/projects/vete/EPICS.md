# Vete Epics

**Project:** [Vete](PROJECT.md)  
**Branch:** `feature/autonomous-improvements` (PR #39)

---

## Epic Summary

| ID | Epic | Status | Stories | Progress |
|----|------|--------|---------|----------|
| EPIC-V001 | Foundation | ✅ Done | 4/4 | 100% |
| EPIC-V002 | Test Coverage | ✅ Done | 3/3 | 100% |
| EPIC-V003 | Security & DevOps | ⏳ Active | 0/4 | 0% |
| EPIC-V004 | Code Quality | 📋 Ready | 0/3 | 0% |
| EPIC-V005 | Production Polish | ⬜ Backlog | 0/4 | 0% |
| EPIC-V006 | Feature Complete MVP | ⬜ Backlog | 0/5 | 0% |

---

## ✅ EPIC-V001: Foundation

_Completed 2026-02-05 (PR #38 merged)_

**Goal:** Establish test infrastructure and patterns.

| Story | Status |
|-------|--------|
| VETE-S-001: API test infrastructure | ✅ |
| VETE-S-002: Auth helpers & fixtures | ✅ |
| VETE-S-003: Integration test framework | ✅ |
| VETE-S-004: Domain patterns introduced | ✅ |

**Deliverables:**
- `vitest.api.setup.ts`
- `CleanupManager` with checkpoint pattern
- 140 CRUD integration tests
- Domain service pattern

---

## ✅ EPIC-V002: Test Coverage

_Completed 2026-02-06_

**Goal:** Fix API tests and increase coverage.

| Story | Status |
|-------|--------|
| VETE-S-005: Fix API test root causes | ✅ |
| VETE-S-006: Reduce lint warnings | ✅ |
| VETE-S-007: Fix domain tests (pets, vaccines, slots) | ✅ |

**Results:**
- API tests: 0% → 46% (292/628)
- Lint: 116 → 96 warnings
- Checkpoint pattern implemented

---

## ⏳ EPIC-V003: Security & DevOps

_Current focus_

**Goal:** Harden security and establish CI/CD.

| Story | Status | Tasks |
|-------|--------|-------|
| VETE-S-008: CI/CD Pipeline | 📋 Ready | 3 |
| VETE-S-009: API Rate Limiting | 📋 Ready | 2 |
| VETE-S-010: Input Sanitization | 📋 Ready | 2 |
| VETE-S-011: Auth Hardening | 📋 Ready | 2 |

→ [Stories & tasks in STORIES.md](STORIES.md)

---

## 📋 EPIC-V004: Code Quality

**Goal:** Clean up tech debt.

| Story | Status | Tasks |
|-------|--------|-------|
| VETE-S-012: Eliminate `any` types | 📋 Ready | — |
| VETE-S-013: Clear lint warnings | 📋 Ready | — |
| VETE-S-014: Reduce context providers | 📋 Ready | — |

---

## ⬜ EPIC-V005: Production Polish

**Goal:** Production-ready quality.

| Story | Status |
|-------|--------|
| VETE-S-015: Dependency updates | ⬜ Backlog |
| VETE-S-016: SEO & meta tags | ⬜ Backlog |
| VETE-S-017: README & dev docs | ⬜ Backlog |
| VETE-S-018: Performance audit | ⬜ Backlog |

---

## ⬜ EPIC-V006: Feature Complete MVP

**Goal:** All core features working.

| Story | Status |
|-------|--------|
| VETE-S-019: Complete appointment flow | ⬜ Backlog |
| VETE-S-020: Inventory management | ⬜ Backlog |
| VETE-S-021: Billing basics | ⬜ Backlog |
| VETE-S-022: Reporting dashboard | ⬜ Backlog |
| VETE-S-023: Multi-language (ES/EN) | ⬜ Backlog |

---

## Velocity

| Week | Epics Completed | Notes |
|------|-----------------|-------|
| 2026-02-05 | EPIC-V001 | Foundation (30 commits) |
| 2026-02-06 | EPIC-V002 | Test coverage + swarm setup |
