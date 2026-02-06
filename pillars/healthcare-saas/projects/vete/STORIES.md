# Vete User Stories

**Project:** [Vete](PROJECT.md)

---

## Active Epic: EPIC-V003 (Security & DevOps)

---

### VETE-S-008: CI/CD Pipeline

**As a** developer  
**I want** tests to run automatically on every PR  
**So that** I catch bugs before they reach main

**Acceptance Criteria:**
- [ ] GitHub Actions workflow runs on push/PR
- [ ] Unit tests run in CI
- [ ] API tests run in CI
- [ ] PR blocked if tests fail

**Tasks:**
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| VETE-T-001 | Create GH Actions workflow | 2h | ⬜ | — |
| VETE-T-002 | Configure test matrix (Node versions) | 1h | ⬜ | — |
| VETE-T-003 | Add branch protection rules | 30m | ⬜ | — |

---

### VETE-S-009: API Rate Limiting

**As a** system  
**I want** rate limiting on public endpoints  
**So that** the API can't be abused

**Acceptance Criteria:**
- [ ] Rate limiter middleware added
- [ ] Configurable limits per endpoint
- [ ] 429 response when exceeded
- [ ] Logged for monitoring

**Tasks:**
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| VETE-T-004 | Research Next.js rate limiting options | 1h | ⬜ | — |
| VETE-T-005 | Implement rate limiter middleware | 3h | ⬜ | — |

---

### VETE-S-010: Input Sanitization

**As a** system  
**I want** all user inputs validated and sanitized  
**So that** the app is protected from injection attacks

**Acceptance Criteria:**
- [ ] All form inputs validated
- [ ] SQL injection prevention verified
- [ ] XSS prevention verified
- [ ] Zod schemas for all API inputs

**Tasks:**
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| VETE-T-006 | Audit all API routes for input handling | 2h | ⬜ | — |
| VETE-T-007 | Add Zod schemas where missing | 4h | ⬜ | — |

---

### VETE-S-011: Auth Hardening

**As a** user  
**I want** my account to be secure  
**So that** my data is protected

**Acceptance Criteria:**
- [ ] Token expiry reviewed
- [ ] Refresh token rotation
- [ ] Session invalidation on password change
- [ ] Failed login attempt logging

**Tasks:**
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| VETE-T-008 | Review Supabase auth configuration | 1h | ⬜ | — |
| VETE-T-009 | Add failed login monitoring | 2h | ⬜ | — |

---

## Ready Stories (EPIC-V004)

### VETE-S-012: Eliminate `any` Types

**As a** developer  
**I want** proper types everywhere  
**So that** TypeScript catches bugs

**Metric:** 99 → <30 `any` occurrences

---

### VETE-S-013: Clear Lint Warnings

**As a** developer  
**I want** zero lint warnings  
**So that** code quality is consistent

**Metric:** 96 → 0 warnings

---

### VETE-S-014: Reduce Context Providers

**As a** developer  
**I want** fewer nested providers  
**So that** the component tree is cleaner

---

## Backlog Stories

_See [EPICS.md](EPICS.md) for EPIC-V005 and EPIC-V006 stories_

---

## Story Template

```markdown
### {REPO}-S-XXX: {Title}

**As a** {who}  
**I want** {what}  
**So that** {why}

**Acceptance Criteria:**
- [ ] Criterion 1
- [ ] Criterion 2

**Tasks:**
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| {REPO}-T-XXX | Task description | Xh | ⬜ | — |
```
