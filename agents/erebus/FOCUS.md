# Erebus 🔥

**Research agent** — ai-whisperers-server

---

## Current Focus

**Project:** p-adic Bioinformatics  
**Path:** `pillars/research/projects/padic-bioinformatics/`

### Priority Order

1. **3-adic-ml** — Add infrastructure (LICENSE, CI, pyproject)
2. **ternary-vaes-bioinformatics** — Run tests, clear TODOs
3. **ultrametric-antigen-AI** — Document, audit

---

## Ready Tasks

Research project needs story files created. Start with:

| Repo | Task | Effort |
|------|------|--------|
| 3-adic-ml | Add LICENSE (MIT) | 15m |
| 3-adic-ml | Create pyproject.toml | 1h |
| 3-adic-ml | Set up GitHub Actions CI | 2h |
| 3-adic-ml | Run tests, document results | 1h |

---

## Workflow

### On Heartbeat

```markdown
1. git pull work-coordination
2. Check TRACKER.md for urgent items
3. Check research project for ready tasks
4. If no claimed task, claim one or create stories
5. Work on claimed task
6. Mark done when complete
```

### Creating Stories

Research project needs story files. Template:

```markdown
# S001: 3-adic-ml Infrastructure

**Epic:** research-setup
**Status:** 📋 Ready

## User Story
As a researcher, I want 3-adic-ml to have proper packaging...

## Tasks
| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Add LICENSE | 15m | ⬜ | — |
| T002 | Create pyproject.toml | 1h | ⬜ | — |
```

---

## Repos

| Repo | Local Path | Priority |
|------|------------|----------|
| 3-adic-ml | `/home/ai-whisperers/3-adic-ml` | HIGH |
| ternary-vaes-bioinformatics | `/home/ai-whisperers/ternary-vaes-bioinformatics` | HIGH |
| ultrametric-antigen-AI | `/home/ai-whisperers/ultrametric-antigen-AI` | HIGH |

---

## Cron Jobs

| Job | Interval | Purpose |
|-----|----------|---------|
| erebus-worker | 20min | Research autonomous work |

---

## Paths

| What | Path |
|------|------|
| Workspace | `~/.openclaw/workspace-erebus/` |
| work-coordination | `/home/ai-whisperers/work-coordination/` |

---

## Notes

- Research repos need Python environment setup
- Run tests in virtualenv
- Document any failures or issues found
