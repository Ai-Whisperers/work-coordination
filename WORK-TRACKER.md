# Work Tracker
_Central task queue for AI Whisperers agents_

Last updated: 2026-02-06 17:30 UTC

---

## Active Epics

| Epic | Owner | Status | Priority | Tracker |
|------|-------|--------|----------|---------|
| [EPIC-001](epics/EPIC-001-vete.md) | Nyx 🌙 | In Progress | HIGH | Vete production readiness |
| [EPIC-010](epics/EPIC-010-ternary-vaes.md) | Erebus 🔥 | Ready | HIGH | ternary-vaes-bioinformatics |
| [EPIC-011](epics/EPIC-011-ultrametric-antigen.md) | Erebus 🔥 | Ready | HIGH | ultrametric-antigen-AI |
| [EPIC-012](epics/EPIC-012-3-adic-ml.md) | Erebus 🔥 | Ready | HIGH | 3-adic-ml |
| [EPIC-003](epics/EPIC-003-infra.md) | Atlas 🗼 | New | MEDIUM | Org infrastructure |

---

## 🔥 EREBUS TASK QUEUE (Research Repos)

### Immediate (Start Here)

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| 3AM-INFRA-001 | Add LICENSE file (MIT) | 3-adic-ml | LOW | ⬜ |
| 3AM-INFRA-002 | Create pyproject.toml | 3-adic-ml | MEDIUM | ⬜ |
| 3AM-INFRA-003 | Set up GitHub Actions CI | 3-adic-ml | MEDIUM | ⬜ |
| 3AM-TEST-001 | Run existing tests, document results | 3-adic-ml | LOW | ⬜ |

### Next Up

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| TVB-DOC-004 | Add .env.example | ternary-vaes-bioinformatics | LOW | ⬜ |
| TVB-TEST-002 | Run full test suite | ternary-vaes-bioinformatics | LOW | ⬜ |
| TVB-QUAL-001 | Fix 2 TODOs in code | ternary-vaes-bioinformatics | LOW | ⬜ |
| UAA-DIFF-001 | Document relationship to ternary-vaes | ultrametric-antigen-AI | LOW | ⬜ |

### Backlog

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| 3AM-DOC-001 | Review and enhance README | 3-adic-ml | LOW | ⬜ |
| 3AM-DOC-002 | Document mathematical foundations | 3-adic-ml | HIGH | ⬜ |
| TVB-DOC-001 | Review and update README | ternary-vaes-bioinformatics | LOW | ⬜ |
| TVB-DOC-002 | Add architecture diagram | ternary-vaes-bioinformatics | MEDIUM | ⬜ |
| UAA-DOC-001 | Review and update README | ultrametric-antigen-AI | LOW | ⬜ |
| UAA-DOC-002 | Document antigen analysis workflow | ultrametric-antigen-AI | MEDIUM | ⬜ |

---

## 🌙 NYX TASK QUEUE (Vete + Infrastructure)

### In Progress

| ID | Task | Repo | Status |
|----|------|------|--------|
| EPIC-001 | Vete workplan (Phase 3+) | Vete | ⏳ Nyx 🌙 |

### Queue

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| T-001 | Fix credential leak (Groq, Langfuse) | LangAi | LOW | ⬜ |
| T-002 | Fix failing CI runs | Vete | MEDIUM | ⬜ |

See `/home/ai-whisperers/.openclaw/workspace/vete-workplan.md` for full Vete task breakdown.

---

## 🗼 ATLAS TASK QUEUE (Pending Setup)

_Atlas will pick up tasks after Jonathan completes setup_

| ID | Task | Repo | Effort | Status |
|----|------|------|--------|--------|
| T-012 | Create org-wide PR template | .github | LOW | ⬜ |
| T-011 | Set up Dependabot org-wide | .github | LOW | ⬜ |

---

## Completed Today

| ID | Task | Agent | Completed | Notes |
|----|------|-------|-----------|-------|
| — | Clone research repos | Nyx 🌙 | 2026-02-06 17:28 | ternary-vaes, ultrametric, 3-adic-ml |
| — | Create Erebus epics | Nyx 🌙 | 2026-02-06 17:30 | EPIC-010, 011, 012 |
| — | Swarm architecture | Nyx 🌙 | 2026-02-06 16:55 | Multi-device coordination |
| — | Erebus setup | Nyx 🌙 | 2026-02-06 16:34 | Workspace + config |
| — | Google Suite setup | Nyx 🌙 | 2026-02-06 16:52 | Gmail/Calendar/Drive |

---

## Claiming Protocol

```
1. git pull origin main
2. Find unclaimed task (⬜ with no agent name)
3. Change to: ⏳ AgentName 🔥
4. git commit -m "claim: TASK-ID by Agent"
5. git push (if fails, someone else claimed - try another)
6. Do the work
7. Change to: ✅ AgentName 🔥 @TIMESTAMP
8. git push
```

---

## Task Format

```
| ID | Task | Repo | Effort | Status |
```

- **Effort:** `LOW` (<1h), `MEDIUM` (1-4h), `HIGH` (4h+)
- **Status:** `⬜` unclaimed, `⏳ Agent` in progress, `✅ Agent @time` done, `🔴 Agent` blocked
