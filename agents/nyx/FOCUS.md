# Nyx 🌙

**Primary agent** — ai-whisperers-server

---

## Current Focus

**Project:** Vete  
**Epic:** v003-security-devops  
**Path:** `pillars/healthcare-saas/projects/vete/epics/v003-security-devops/`

### Ready Tasks

| Story | Task | Effort |
|-------|------|--------|
| s001 | T001: GH Actions workflow | 2h |
| s001 | T002: Node matrix | 30m |
| s001 | T003: Branch protection | 30m |
| s002 | T001: Research rate limiting | 1h |
| s002 | T002: Implement rate limiter | 3h |
| s003 | T001: Audit API routes | 2h |
| s003 | T002: Add Zod schemas | 4h |
| s004 | T001: Review Supabase auth | 1h |
| s004 | T002: Failed login monitoring | 2h |

---

## Workflow

### On Heartbeat

```markdown
1. git pull work-coordination
2. Check TRACKER.md for urgent items
3. Check v003 epic for ready tasks
4. If no claimed task, claim one
5. Work on claimed task
6. Mark done when complete
```

### Claiming

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
# Edit: pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md
# Change task row: ⬜ | — → ⏳ | Nyx 🌙
git commit -m "claim: VETE-v003-s001-T001 by Nyx"
git push origin main
```

### Working

```bash
cd /home/ai-whisperers/Vete/web
# Do the actual work
# Commit to Vete repo
```

### Completing

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
# Edit story file: ⏳ → ✅
# Check off acceptance criteria
git commit -m "done: VETE-v003-s001-T001"
git push origin main
```

---

## Cron Jobs

| Job | Interval | Purpose |
|-----|----------|---------|
| group-poller | 5min | Poll WhatsApp groups |
| vete-worker | 15min | Autonomous Vete work |
| vete-qa | 20min | Code review |
| server-health | 30min | Server checks |

---

## Paths

| What | Path |
|------|------|
| Workspace | `~/.openclaw/workspace/` |
| work-coordination | `/home/ai-whisperers/work-coordination/` |
| Vete | `/home/ai-whisperers/Vete/web/` |
| Vete workplan | `~/.openclaw/workspace/vete-workplan.md` |

---

## Sub-Agents

Use Sonnet sub-agents for mechanical tasks:

```
sessions_spawn(
  task="Fix any types in lib/domains/pets/",
  model="anthropic/claude-sonnet-4-20250514"
)
```

Good for:
- Fixing lint warnings
- Adding types
- Writing tests
- Documentation
