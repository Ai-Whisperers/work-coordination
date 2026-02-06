# AI Whisperers Work Coordination

Central hub for the AI agent swarm.

---

## Quick Start

| I want to... | Go to... |
|--------------|----------|
| See what's active | [TRACKER.md](TRACKER.md) |
| Claim a task | Story file in `pillars/.../epics/.../s00X-*.md` |
| Understand the system | [HIERARCHY.md](HIERARCHY.md) |
| Set up new agent | [templates/SETUP-ATLAS.md](templates/SETUP-ATLAS.md) |

---

## Structure

```
work-coordination/
│
├── TRACKER.md              # 📊 Dashboard
├── HIERARCHY.md            # 📐 Definitions
│
├── pillars/                # All work organized here
│   ├── _index.md          # Pillar overview
│   │
│   └── healthcare-saas/projects/vete/
│       ├── _project.md    # Project overview
│       ├── _backlog.md    # Ideas
│       │
│       └── epics/
│           └── v003-security-devops/   # Active epic
│               ├── _epic.md            # Epic definition
│               ├── s001-cicd-pipeline.md    # Story + tasks
│               ├── s002-rate-limiting.md
│               └── ...
│
├── agents/                # Agent registry
└── templates/             # Setup guides
```

---

## Hierarchy

```
COMPANY
  └── PILLAR (strategic direction)
        └── PROJECT (business initiative)  
              └── REPO (code artifact)
                    └── EPIC (large deliverable) = folder
                          └── STORY (outcome) = file
                                └── TASK (work unit) = checklist item
```

**Agents claim tasks.** Tasks live inside story files.

---

## Agents

| Agent | Status | Focus |
|-------|--------|-------|
| Nyx 🌙 | ✅ | Vete |
| Erebus 🔥 | ✅ | Research |
| Atlas 🗼 | ⏳ | Pending |

---

## Claiming Work

```bash
# 1. Find a task in a story file
# 2. Edit the task row: ⬜ | — → ⏳ | YourName

git pull
vim pillars/.../s001-cicd-pipeline.md
git commit -m "claim: VETE-v003-s001-T001 by Nyx"
git push

# 3. If push fails, someone else got it
# 4. Do the work on the actual repo
# 5. Mark done: ⏳ → ✅
```

---

## Pillars

| # | Pillar | Status |
|---|--------|--------|
| 1 | Healthcare SaaS | 🟢 Active |
| 2 | Research | 🟡 Maintenance |
| 3 | Education | ⚪ Paused |
| 4 | Tools & Infra | 🟢 Active |

---

_[AI Whisperers](https://github.com/Ai-Whisperers)_
