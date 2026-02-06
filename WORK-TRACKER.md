# Work Tracker
_Central task queue for AI Whisperers agents_

Last updated: 2026-02-06 16:56 UTC

---

## Active Epics

| Epic | Owner | Status | Tracker |
|------|-------|--------|---------|
| [EPIC-001](epics/EPIC-001-vete.md) | Nyx 🌙 | In Progress | Vete production readiness |
| [EPIC-002](epics/EPIC-002-research.md) | Erebus 🔥 | New | Research repos audit |
| [EPIC-003](epics/EPIC-003-infra.md) | Shared | New | Org-wide infrastructure |

---

## Task Queue

### 🔴 High Priority

| ID | Task | Repo | Type | Effort | Assigned |
|----|------|------|------|--------|----------|
| T-001 | Fix credential leak (Groq, Langfuse) | LangAi | security | LOW | |
| T-002 | Fix failing CI runs | Vete | bug | MEDIUM | |
| T-003 | Add .env.example to repos missing it | multiple | infra | LOW | |

### 🟡 Medium Priority

| ID | Task | Repo | Type | Effort | Assigned |
|----|------|------|------|--------|----------|
| T-010 | Add README to research repos | research/* | docs | LOW | |
| T-011 | Set up Dependabot org-wide | .github | infra | LOW | |
| T-012 | Create PR/issue templates | .github | infra | LOW | |
| T-013 | Document ternary-vaes architecture | ternary-vaes | docs | MEDIUM | |

### 🟢 Low Priority / Backlog

| ID | Task | Repo | Type | Effort | Assigned |
|----|------|------|------|--------|----------|
| T-020 | Docker setup for Vete | Vete | infra | HIGH | |
| T-021 | Storybook for UI components | Vete | dx | HIGH | |
| T-022 | API documentation (OpenAPI) | Vete | docs | MEDIUM | |

---

## In Progress

| ID | Task | Agent | Started | Branch/PR |
|----|------|-------|---------|-----------|
| EPIC-001 | Vete workplan (Phase 3+) | Nyx 🌙 | 2026-02-05 | feature/autonomous-improvements |

---

## Completed (Recent)

| ID | Task | Agent | Completed | Notes |
|----|------|-------|-----------|-------|
| — | Erebus setup | Nyx 🌙 | 2026-02-06 16:34 | Workspace + config |
| — | Telegram enabled | Nyx 🌙 | 2026-02-06 16:36 | @AI_whisperBot |
| — | Google Suite setup | Nyx 🌙 | 2026-02-06 16:52 | Gmail/Calendar/Drive |
| — | Swarm architecture | Nyx 🌙 | 2026-02-06 16:55 | Multi-device coordination |

---

## Claiming Tasks

1. Pull latest: `git pull origin main`
2. Find unclaimed task (no agent in Assigned column)
3. Add your name: `⏳ AgentName` 
4. Commit & push immediately
5. If push fails, pull and try another task
6. When done: change to `✅ AgentName @TIMESTAMP`

---

## Adding Tasks

Use this format:
```
| T-XXX | Brief description | repo-name | type | effort | |
```

**Types:** `bug`, `feature`, `docs`, `infra`, `security`, `test`, `dx`  
**Effort:** `LOW` (<1h), `MEDIUM` (1-4h), `HIGH` (4h+)
