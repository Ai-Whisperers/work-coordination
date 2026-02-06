# 📊 Work Tracker

_Dashboard view of all active work_

**Updated:** 2026-02-06 18:15 UTC

---

## 🚨 Urgent

| Issue | Location | Owner |
|-------|----------|-------|
| Groq API key exposed | `LangAi/update_env.py:19` | ⬜ |
| Langfuse creds exposed | `LangAi/update_env.py:33` | ⬜ |

---

## Pillar Health

| Pillar | Status | Active Project | Current Epic |
|--------|--------|----------------|--------------|
| [Healthcare SaaS](pillars/healthcare-saas/) | 🟢 | Vete | v003-security-devops |
| [Research](pillars/research/) | 🟡 | p-adic Bio | — (needs setup) |
| [Education](pillars/education/) | ⚪ | — | Paused |
| [Tools & Infra](pillars/tools-infra/) | 🟢 | Org standards | — |

---

## Agent Status

| Agent | Status | Working On |
|-------|--------|------------|
| Nyx 🌙 | ✅ Active | Vete v003 |
| Erebus 🔥 | ✅ Active | Research setup |
| Atlas 🗼 | ⏳ Pending | Needs install |

---

## 📋 Ready to Claim

### Vete — v003-security-devops

| Story | Task | Effort | File |
|-------|------|--------|------|
| s001 | T001: Create GH Actions workflow | 2h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md) |
| s001 | T002: Configure Node matrix | 30m | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md) |
| s001 | T003: Branch protection rules | 30m | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md) |
| s002 | T001: Research rate limiting | 1h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s002-rate-limiting.md) |
| s002 | T002: Implement rate limiter | 3h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s002-rate-limiting.md) |
| s003 | T001: Audit API routes | 2h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s003-input-sanitization.md) |
| s003 | T002: Add Zod schemas | 4h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s003-input-sanitization.md) |
| s004 | T001: Review Supabase auth | 1h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s004-auth-hardening.md) |
| s004 | T002: Failed login monitoring | 2h | [→](pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s004-auth-hardening.md) |

**Total:** 9 tasks, ~16h of work

---

## 📈 Progress

### Vete

| Epic | Status | Progress |
|------|--------|----------|
| v001-foundation | ✅ | 100% |
| v002-test-coverage | ✅ | 100% |
| v003-security-devops | ⏳ | 0% (0/9 tasks) |
| v004-code-quality | 📋 | Not started |
| v005-production-polish | ⬜ | Backlog |
| v006-feature-mvp | ⬜ | Backlog |

---

## 🗂️ Navigation

```
Start here
    │
    ├── pillars/healthcare-saas/projects/vete/
    │   ├── _project.md          # Project overview
    │   └── epics/v003-.../      # Active epic
    │       ├── _epic.md         # Epic overview  
    │       └── s001-*.md        # Stories with tasks ← CLAIM HERE
    │
    └── agents/
        └── {agent}/FOCUS.md     # What each agent is doing
```

---

## Claiming a Task

1. Find task in story file (e.g., `s001-cicd-pipeline.md`)
2. Edit: `⬜ | —` → `⏳ | Nyx`
3. Commit: `claim: VETE-v003-s001-T001 by Nyx`
4. Push (if fails, someone else claimed it)
5. Do the work on the actual repo
6. Edit: `⏳` → `✅`, add completion time
7. Commit: `done: VETE-v003-s001-T001`
