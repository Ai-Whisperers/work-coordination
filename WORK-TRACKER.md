# Work Tracker
_Central task queue for AI Whisperers agents_

Last updated: 2026-02-06 17:35 UTC

---

## Epic Overview

| Epic | Name | Owner | Priority | Status |
|------|------|-------|----------|--------|
| [EPIC-001](epics/EPIC-001-vete.md) | **Vete** — Veterinary SaaS | Nyx 🌙 | CRITICAL | ⏳ In Progress |
| [EPIC-010](epics/EPIC-010-ternary-vaes.md) | ternary-vaes-bioinformatics | Erebus 🔥 | HIGH | ⬜ Ready |
| [EPIC-011](epics/EPIC-011-ultrametric-antigen.md) | ultrametric-antigen-AI | Erebus 🔥 | HIGH | ⬜ Ready |
| [EPIC-012](epics/EPIC-012-3-adic-ml.md) | 3-adic-ml | Erebus 🔥 | HIGH | ⬜ Ready |
| [EPIC-020](epics/EPIC-020-psicologia-ia.md) | psicologia-ia | Available | MEDIUM | ⬜ New |
| [EPIC-021](epics/EPIC-021-courses-website.md) | courses-website | Available | MEDIUM | ⬜ New |
| [EPIC-022](epics/EPIC-022-langai.md) | **LangAi** (Security!) | Available | HIGH | 🚨 URGENT |
| [EPIC-023](epics/EPIC-023-photos-to-kml.md) | photos-to-kml | Atlas 🗼 | MEDIUM | ⬜ Ready |
| [EPIC-024](epics/EPIC-024-healthcare.md) | Healthcare Templates | Available | LOW | ⬜ New |
| [EPIC-003](epics/EPIC-003-infra.md) | Org Infrastructure | Atlas 🗼 | MEDIUM | ⬜ Ready |

---

## 🚨 URGENT — Security Issues

| ID | Task | Repo | Owner | Status |
|----|------|------|-------|--------|
| LNG-SEC-001 | Remove exposed Groq API key | LangAi | — | ⬜ |
| LNG-SEC-002 | Remove exposed Langfuse creds | LangAi | — | ⬜ |
| LNG-SEC-003 | Add .env.example | LangAi | — | ⬜ |

---

## 🌙 NYX — Vete Tasks

**Epic:** EPIC-001 | **Branch:** `feature/autonomous-improvements`

### Current Phase: Security & DevOps

| ID | Task | Effort | Status |
|----|------|--------|--------|
| VETE-SEC-001 | API Rate Limiting | MEDIUM | ⬜ |
| VETE-SEC-002 | Input Sanitization Audit | MEDIUM | ⬜ |
| VETE-SEC-003 | Auth & Session Security Review | LOW | ⬜ |
| VETE-DEV-001 | GitHub Actions CI Pipeline | MEDIUM | ⬜ |
| VETE-DEV-002 | Add .env.example | LOW | ⬜ |
| VETE-DEV-003 | Docker Development Environment | MEDIUM | ⬜ |

### Backlog

| ID | Task | Effort | Status |
|----|------|--------|--------|
| VETE-ARCH-001 | Reduce Context Provider Sprawl | HIGH | ⬜ |
| VETE-ARCH-002 | Domain Pattern Migration | HIGH | ⬜ |
| VETE-PROD-001 | Dependency Updates | LOW | ⬜ |
| VETE-PROD-002 | Console Statement Cleanup | LOW | ⬜ |
| VETE-PROD-003 | SEO & Meta Tags | LOW | ⬜ |
| VETE-PROD-004 | README & Developer Docs | LOW | ⬜ |

**Full task breakdown:** `/home/ai-whisperers/.openclaw/workspace/vete-workplan.md`

---

## 🔥 EREBUS — Research Repos

**Focus:** 3 repos only (3-adic-ml → ternary-vaes → ultrametric)

### Immediate (Start with 3-adic-ml)

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| 3AM-INFRA-001 | Add LICENSE file (MIT) | 3-adic-ml | LOW | ⬜ |
| 3AM-INFRA-002 | Create pyproject.toml | 3-adic-ml | MEDIUM | ⬜ |
| 3AM-INFRA-003 | Set up GitHub Actions CI | 3-adic-ml | MEDIUM | ⬜ |
| 3AM-TEST-001 | Run existing tests | 3-adic-ml | LOW | ⬜ |

### Next (ternary-vaes-bioinformatics)

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| TVB-DOC-004 | Add .env.example | ternary-vaes | LOW | ⬜ |
| TVB-TEST-002 | Run full test suite | ternary-vaes | LOW | ⬜ |
| TVB-QUAL-001 | Fix 2 TODOs in code | ternary-vaes | LOW | ⬜ |

### Later (ultrametric-antigen-AI)

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| UAA-DIFF-001 | Document relationship to ternary-vaes | ultrametric | LOW | ⬜ |
| UAA-DOC-001 | Review and update README | ultrametric | LOW | ⬜ |

---

## 🗼 ATLAS — General + John's Projects

**Status:** Pending setup (Jonathan)

### Assigned

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| PTK-FEAT-001 | Audit photos-to-kml functionality | photos-to-kml | LOW | ⬜ |
| ORG-TMPL-001 | Create PR template | .github | LOW | ⬜ |
| ORG-CI-003 | Set up Dependabot for org | .github | LOW | ⬜ |

---

## 📋 AVAILABLE — Unclaimed Tasks

_Any agent can claim these_

### High Priority

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| LNG-SEC-001 | Remove exposed Groq API key | LangAi | LOW | ⬜ |
| LNG-SEC-002 | Remove exposed Langfuse creds | LangAi | LOW | ⬜ |

### Medium Priority

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| PSI-DOC-001 | Review README | psicologia-ia | LOW | ⬜ |
| CRS-DOC-001 | Review README | courses-website | LOW | ⬜ |
| FIS-DOC-001 | Add README | mikie-fisio | LOW | ⬜ |
| ODO-DOC-001 | Add README | Odontology | LOW | ⬜ |

---

## In Progress

| ID | Task | Agent | Started | Notes |
|----|------|-------|---------|-------|
| EPIC-001 | Vete Phase 3+ | Nyx 🌙 | 2026-02-05 | Via vete-workplan.md |

---

## Completed Today

| ID | Task | Agent | Time |
|----|------|-------|------|
| — | Create all epics | Nyx 🌙 | 17:35 |
| — | Clone research repos | Nyx 🌙 | 17:28 |
| — | Clone business repos | Nyx 🌙 | 17:31 |
| — | Swarm architecture | Nyx 🌙 | 16:55 |
| — | Erebus setup | Nyx 🌙 | 16:34 |
| — | Google Suite setup | Nyx 🌙 | 16:52 |

---

## Claiming Protocol

```bash
git pull origin main
# Edit this file - change ⬜ to ⏳ YourName
git commit -m "claim: TASK-ID by Agent"
git push origin main
# If push fails, pull and try another task
# When done: change ⏳ to ✅ YourName @TIMESTAMP
```

---

## Legend

- ⬜ — Unclaimed/Ready
- ⏳ — In Progress (+ Agent name)
- ✅ — Complete (+ Agent + timestamp)
- 🔴 — Blocked (+ reason)
- 🚨 — Urgent/Security
