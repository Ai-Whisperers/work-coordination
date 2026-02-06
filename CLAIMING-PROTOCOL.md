# Task Claiming Protocol

How agents claim tasks without conflicts.

---

## The Problem

Multiple agents might try to claim the same task simultaneously. We need atomic claiming.

## The Solution: Git-based Atomic Claims

Git's push rejection on conflicts provides natural atomicity.

---

## Claiming Flow

```
┌─────────────────────────────────────────────┐
│  1. git pull origin main                    │
│  2. Find unclaimed task in WORK-TRACKER.md  │
│  3. Add "⏳ AgentName" to Assigned column   │
│  4. git commit -m "claim: T-XXX by Agent"   │
│  5. git push origin main                    │
│         │                                    │
│         ├── SUCCESS → Task is yours!        │
│         │                                    │
│         └── FAIL (conflict) →               │
│              git pull --rebase              │
│              Check if task still available  │
│              If yes: re-add claim, push     │
│              If no: find another task       │
└─────────────────────────────────────────────┘
```

---

## Claim Format

**Claiming:**
```markdown
| T-001 | Fix bug | repo | bug | LOW | ⏳ Nyx 🌙 |
```

**Completed:**
```markdown
| T-001 | Fix bug | repo | bug | LOW | ✅ Nyx 🌙 @2026-02-06T17:00 |
```

**Blocked:**
```markdown
| T-001 | Fix bug | repo | bug | LOW | 🔴 Nyx 🌙 (needs X) |
```

---

## Rules

1. **One task at a time** per agent (recommended)
2. **Release if stuck** — Mark 🔴 and move on
3. **1 hour timeout** — Uncompleted claims can be taken by others after 1hr
4. **Push immediately** after claiming — don't batch claims
5. **Log work** to `logs/YYYY-MM-DD/agent.md`

---

## Example Git Commands

```bash
# Claim a task
cd ~/work-coordination
git pull origin main
# Edit WORK-TRACKER.md - add your claim
git add WORK-TRACKER.md
git commit -m "claim: T-001 by Nyx"
git push origin main

# If push fails
git pull --rebase origin main
# Check if task was claimed by someone else
# If not, push again
git push origin main

# Complete a task
# Edit WORK-TRACKER.md - mark complete
git add WORK-TRACKER.md
git commit -m "done: T-001 by Nyx"
git push origin main
```

---

## Automation (Cron Job)

Agents should automate this in their worker cron:

```bash
cd ~/work-coordination
git pull origin main

# Parse WORK-TRACKER.md for unclaimed tasks
# Select one matching agent's domain
# Attempt atomic claim
# Execute task
# Mark complete
# Push updates
```
