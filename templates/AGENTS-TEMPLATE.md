# AGENTS.md — {AgentName}

_Template for agent workspace AGENTS.md. Copy to workspace and customize._

---

## First Run

If `BOOTSTRAP.md` exists, follow it, then delete it.

## Every Session

1. Read `SOUL.md` — who you are
2. Read `USER.md` — who you're helping
3. Read `memory/YYYY-MM-DD.md` (today + yesterday)
4. If main session: Read `MEMORY.md`

---

## Work Coordination

All work is tracked in: `/home/ai-whisperers/work-coordination/`

### Finding Work

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main

# Option 1: Dashboard
cat TRACKER.md

# Option 2: Your domain
ls pillars/{your-pillar}/projects/{your-project}/epics/

# Option 3: Find unclaimed
grep -r "⬜ | —" pillars/
```

### Claiming Work

```bash
# Edit story file: ⬜ | — → ⏳ | {YourName}
git commit -am "claim: PROJ-epic-story-TASK by {Agent}"
git push origin main
# If push fails, someone else claimed. Pick another.
```

### Doing Work

Work on the **actual repo**, not work-coordination:
```bash
cd /home/ai-whisperers/{Repo}
# Do the work
# Commit there
```

### Completing Work

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
# Edit story file: ⏳ → ✅, check acceptance criteria
git commit -am "done: PROJ-epic-story-TASK"
git push origin main
```

---

## File Hierarchy

```
pillars/
└── {pillar}/
    └── projects/
        └── {project}/
            ├── _project.md      # Overview
            ├── _backlog.md      # Ideas
            └── epics/
                └── {epic}/
                    ├── _epic.md     # Epic definition
                    └── s00X-*.md    # Story files (tasks inside)
```

---

## Task IDs

```
{PROJECT}-{EPIC}-{STORY}-{TASK}
VETE-v003-s001-T001
```

---

## Status Icons

| Icon | Meaning |
|------|---------|
| ⬜ | Ready to claim |
| ⏳ | In progress |
| ✅ | Complete |
| 🔴 | Blocked |

---

## Memory

- Daily notes: `memory/YYYY-MM-DD.md`
- Long-term: `MEMORY.md` (main session only)
- Write it down — no "mental notes"

---

## Safety

- Don't exfiltrate data
- `trash` > `rm`
- Ask before external actions (email, posts)
