# Work Tracker

_Central task queue for AI Whisperers agents_

**Last updated:** 2026-02-06 17:50 UTC

---

## 🚨 URGENT

| ID | Task | Domain | Owner | Status |
|----|------|--------|-------|--------|
| LNG-SEC-001 | Remove Groq API key | [tools/](domains/tools/) | — | ⬜ |
| LNG-SEC-002 | Remove Langfuse creds | [tools/](domains/tools/) | — | ⬜ |

→ See [domains/tools/](domains/tools/) for details.

---

## Domain Overview

| Domain | Owner | Priority | Active Tasks | Link |
|--------|-------|----------|--------------|------|
| **Flagship (Vete)** | Nyx 🌙 | CRITICAL | ⏳ Ongoing | [→](domains/flagship/vete/) |
| **Research** | Erebus 🔥 | HIGH | ⬜ Ready | [→](domains/research/) |
| **Tools** | — | HIGH | 🚨 Security | [→](domains/tools/) |
| **Infrastructure** | Atlas 🗼 | MEDIUM | ⬜ Ready | [→](infrastructure/) |
| **Healthcare** | — | LOW | ⬜ Backlog | [→](domains/healthcare/) |
| **Education** | — | LOW | ⬜ Backlog | [→](domains/education/) |
| **Marketing** | — | LOW | ⬜ Backlog | [→](domains/marketing/) |

---

## 🌙 Nyx — Active

**Domain:** Flagship / Vete

| ID | Task | Status | Notes |
|----|------|--------|-------|
| VETE-PHASE3 | Security & DevOps | ⏳ | See [vete/TASKS.md](domains/flagship/vete/TASKS.md) |

**Cron workers:** vete-worker (15min), vete-qa (20min)

---

## 🔥 Erebus — Ready

**Domain:** Research

| ID | Task | Status | Notes |
|----|------|--------|-------|
| 3AM-INFRA | Add LICENSE, pyproject, CI | ⬜ | Start here |
| TVB-TEST | Run tests, clear TODOs | ⬜ | After 3-adic-ml |
| UAA-DOC | Document, audit | ⬜ | After ternary-vaes |

**Cron workers:** erebus-worker (20min)

→ Full details: [domains/research/](domains/research/)

---

## 🗼 Atlas — Pending Setup

**Status:** Waiting for Jonathan to install OpenClaw

**Assigned when ready:**
- PTK-FEAT-001: Audit photos-to-kml
- ORG-TMPL-001: Create PR template

→ Setup guide: [templates/SETUP-ATLAS.md](templates/SETUP-ATLAS.md)

---

## 📋 Available Tasks

_Any agent can claim these_

### High Priority

| ID | Task | Domain | Effort |
|----|------|--------|--------|
| LNG-SEC-001 | Remove Groq API key | Tools | LOW |
| LNG-SEC-002 | Remove Langfuse creds | Tools | LOW |

### Medium Priority

| ID | Task | Domain | Effort |
|----|------|--------|--------|
| ORG-TMPL-001 | Create PR template | Infra | LOW |
| ORG-CI-001 | Reusable Node.js CI | Infra | MEDIUM |

### Low Priority

| ID | Task | Domain | Effort |
|----|------|--------|--------|
| PSI-DOC-001 | Review psicologia-ia README | Healthcare | LOW |
| CRS-DOC-001 | Review courses-website README | Education | LOW |

---

## ✅ Completed Today

| Time | Task | Agent |
|------|------|-------|
| 17:50 | Repo reorganization | Nyx 🌙 |
| 17:35 | Create all epics | Nyx 🌙 |
| 17:28 | Clone research repos | Nyx 🌙 |
| 16:55 | Swarm architecture | Nyx 🌙 |
| 16:34 | Erebus setup | Nyx 🌙 |

---

## Legend

- ⬜ — Unclaimed/Ready
- ⏳ — In Progress (+ Agent)
- ✅ — Complete (+ Agent + time)
- 🔴 — Blocked
- 🚨 — Urgent/Security

---

## Claiming

```bash
git pull origin main
# Edit this file: ⬜ → ⏳ YourName
git commit -m "claim: TASK-ID by Agent"
git push origin main
# Push fails? Someone else claimed. Pick another.
```

→ Full protocol: [CLAIMING-PROTOCOL.md](CLAIMING-PROTOCOL.md)
