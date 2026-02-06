# HEARTBEAT.md — {AgentName}

_Template for agent heartbeat file. Copy to workspace and customize._

---

## On Each Heartbeat

### 1. Check work-coordination

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
```

### 2. Check TRACKER.md

Look for:
- 🚨 Urgent items (security issues, blockers)
- Tasks assigned to you
- Ready tasks in your domain

### 3. Check Your Active Epic

**Your project:** `pillars/{pillar}/projects/{project}/epics/{active-epic}/`

- Any tasks you claimed that need finishing?
- Any ready tasks you can claim?

### 4. Claim or Continue

**If you have a claimed task:**
```
Continue working on it.
```

**If you have no claimed task:**
```bash
# Find unclaimed tasks
grep -r "⬜ | —" pillars/

# Claim one
vim pillars/.../s00X-story.md
# Change: ⬜ | — → ⏳ | {YourName}
git commit -am "claim: PROJ-epic-story-TASK by {Agent}"
git push origin main
```

### 5. Do the Work

Work on the actual repo:
```bash
cd /home/ai-whisperers/{Repo}
# Do the work
# Commit to that repo
```

### 6. Mark Done

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
vim pillars/.../s00X-story.md
# Change: ⏳ → ✅
# Check off acceptance criteria [x]
git commit -am "done: PROJ-epic-story-TASK"
git push origin main
```

---

## If Nothing Needs Attention

Reply: `HEARTBEAT_OK`

---

## Proactive Work

If no urgent tasks, you can:
- Review and update documentation
- Run tests and fix failures
- Improve code quality (lint, types)
- Update MEMORY.md with learnings

---

## Domain Ownership

| Agent | Primary Domain | Path |
|-------|----------------|------|
| Nyx 🌙 | Vete | `pillars/healthcare-saas/projects/vete/` |
| Erebus 🔥 | Research | `pillars/research/projects/padic-bioinformatics/` |
| Atlas 🗼 | General | Any unclaimed |

---

## Polling Groups (if applicable)

```bash
# Check WhatsApp group for messages mentioning you
wacli messages search "{yourname}" --chat "{group_jid}" --after "{last_check}" --limit 10

# Respond via message tool if needed
```
