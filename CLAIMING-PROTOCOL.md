# Claiming Protocol

How AI agents claim and complete work.

---

## Overview

```
1. FIND    → Browse TRACKER.md or dive into epics/
2. CLAIM   → Edit story file, commit, push
3. WORK    → Do the work on the actual repo
4. DONE    → Update story file, commit, push
```

---

## Step 1: Find Work

### Option A: Dashboard
Start at [TRACKER.md](TRACKER.md) → shows ready tasks with links.

### Option B: Direct Browse
```
pillars/
└── {pillar}/projects/{project}/epics/{epic}/
    └── s00X-{story}.md   ← tasks are inside these
```

### Option C: grep
```bash
cd /home/ai-whisperers/work-coordination
grep -r "⬜ | —" pillars/   # Find unclaimed tasks
```

---

## Step 2: Claim a Task

### 2.1 Pull latest
```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
```

### 2.2 Edit the story file

Find the task table in the story file:

**Before:**
```markdown
| T001 | Create GH Actions workflow | 2h | ⬜ | — |
```

**After:**
```markdown
| T001 | Create GH Actions workflow | 2h | ⏳ | Nyx 🌙 |
```

### 2.3 Commit and push
```bash
git add -A
git commit -m "claim: VETE-v003-s001-T001 by Nyx"
git push origin main
```

### 2.4 If push fails
Someone else claimed something. Pull and check:
```bash
git pull origin main
# Check if YOUR task was taken
# If yes, pick a different task
# If no (conflict was elsewhere), resolve and push
```

---

## Step 3: Do the Work

Work happens on the **actual repo**, not work-coordination.

```bash
# Example: Vete task
cd /home/ai-whisperers/Vete/web

# Do the work...
# Commit to the repo...
# Push or create PR...
```

**Important:** The story file has implementation notes in "Task Details" section. Read them.

---

## Step 4: Mark Done

### 4.1 Update the story file

**Before:**
```markdown
| T001 | Create GH Actions workflow | 2h | ⏳ | Nyx 🌙 |
```

**After:**
```markdown
| T001 | Create GH Actions workflow | 2h | ✅ | Nyx 🌙 |
```

### 4.2 Update acceptance criteria
Check off completed items:
```markdown
## Acceptance Criteria
- [x] GitHub Actions runs on push/PR   ← was [ ], now [x]
- [ ] Unit tests run in CI
```

### 4.3 Commit
```bash
git add -A
git commit -m "done: VETE-v003-s001-T001

- Created .github/workflows/ci.yml
- Runs on push and PR to main
- ~2h actual time"
git push origin main
```

---

## Task ID Convention

```
{PROJECT}-{EPIC}-{STORY}-{TASK}
VETE-v003-s001-T001

Where:
- VETE = project
- v003 = epic (v003-security-devops)
- s001 = story (s001-cicd-pipeline)
- T001 = task number
```

---

## Status Icons

| Icon | Meaning | In Table |
|------|---------|----------|
| ⬜ | Ready to claim | `⬜ \| —` |
| ⏳ | In progress | `⏳ \| AgentName` |
| ✅ | Complete | `✅ \| AgentName` |
| 🔴 | Blocked | `🔴 \| reason` |

---

## Story Completion

When ALL tasks in a story are ✅:

1. Check all acceptance criteria are met
2. Update story status at top:
   ```markdown
   **Status:** ✅ Complete
   ```
3. Update epic `_epic.md` progress

---

## Epic Completion

When ALL stories in an epic are ✅:

1. Update `_epic.md`:
   ```markdown
   **Status:** ✅ Complete
   **Completed:** 2026-02-XX
   ```
2. Move story files to `../../_archive/{epic}/` (optional)
3. Update `_project.md` epic table
4. Update `TRACKER.md`

---

## Conflict Resolution

If two agents claim the same task:
- First successful push wins
- Loser picks a different task
- No drama, just move on

If you see someone else's claim but they're inactive:
- Wait 24 hours
- Then you can re-claim with note: `re-claim: was inactive`

---

## Example Full Flow

```bash
# 1. Find work
cd /home/ai-whisperers/work-coordination
cat TRACKER.md  # See what's ready

# 2. Claim
git pull origin main
vim pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md
# Change: ⬜ | — → ⏳ | Nyx 🌙
git commit -am "claim: VETE-v003-s001-T001 by Nyx"
git push origin main

# 3. Work (on actual repo)
cd /home/ai-whisperers/Vete/web
# ... create .github/workflows/ci.yml ...
git add -A
git commit -m "ci: add GitHub Actions workflow"
git push origin feature/ci

# 4. Done
cd /home/ai-whisperers/work-coordination
git pull origin main
vim pillars/healthcare-saas/projects/vete/epics/v003-security-devops/s001-cicd-pipeline.md
# Change: ⏳ | Nyx 🌙 → ✅ | Nyx 🌙
# Check off acceptance criteria
git commit -am "done: VETE-v003-s001-T001"
git push origin main
```
