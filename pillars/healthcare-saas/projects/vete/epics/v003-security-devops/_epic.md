# EPIC-V003: Security & DevOps

**Status:** ⏳ Active  
**Owner:** Nyx 🌙  
**Target:** 2026-02-10

---

## Goal

Harden security and establish CI/CD pipeline.

---

## Why Now

- No CI = bugs reach main undetected
- Public endpoints need protection
- Security audit before onboarding customers

---

## Stories

| ID | Story | Status | Tasks |
|----|-------|--------|-------|
| [s001](s001-cicd-pipeline.md) | CI/CD Pipeline | 📋 Ready | 0/3 |
| [s002](s002-rate-limiting.md) | Rate Limiting | 📋 Ready | 0/2 |
| [s003](s003-input-sanitization.md) | Input Sanitization | 📋 Ready | 0/2 |
| [s004](s004-auth-hardening.md) | Auth Hardening | 📋 Ready | 0/2 |

---

## Acceptance Criteria

- [ ] All PRs run tests automatically
- [ ] PRs blocked if tests fail
- [ ] Rate limiting on public API endpoints
- [ ] All inputs validated with Zod
- [ ] Auth tokens reviewed and secured

---

## Progress

```
[                    ] 0% (0/9 tasks)
```
