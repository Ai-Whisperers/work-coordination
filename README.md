# AI Whisperers Work Coordination 🤖

Central coordination hub for the AI agent swarm.

---

## Quick Start

| I want to... | Go to... |
|--------------|----------|
| See what's happening | [TRACKER.md](TRACKER.md) |
| Claim a task | [pillars/.../TASKS.md](pillars/) |
| Understand the structure | [HIERARCHY.md](HIERARCHY.md) |
| Set up a new agent | [templates/SETUP-ATLAS.md](templates/SETUP-ATLAS.md) |

---

## Structure

```
work-coordination/
│
├── TRACKER.md              # 📊 Dashboard — start here
├── HIERARCHY.md            # 📐 Level definitions
├── CLAIMING-PROTOCOL.md    # 🔒 How to claim tasks
│
├── pillars/                # 📁 All work organized by strategic pillar
│   ├── _index.md          #    Pillar overview
│   │
│   ├── healthcare-saas/   # 🏥 PIL-001 (PRIMARY)
│   │   ├── PILLAR.md
│   │   └── projects/
│   │       └── vete/      #    PRJ-VETE
│   │           ├── PROJECT.md
│   │           ├── EPICS.md
│   │           ├── STORIES.md
│   │           └── TASKS.md   ← Claim tasks here
│   │
│   ├── research/          # 🔬 PIL-002
│   │   └── projects/
│   │       └── padic-bioinformatics/
│   │
│   ├── education/         # 📚 PIL-003 (paused)
│   └── tools-infra/       # 🛠️ PIL-004
│
├── agents/                # 🤖 Agent registry & focus
│   ├── nyx/
│   ├── erebus/
│   └── atlas/
│
├── templates/             # 📝 Setup templates
├── archive/               # 📦 Completed/deprecated
└── domains/               # (legacy, see pillars/)
```

---

## Hierarchy

```
COMPANY (Ai-Whisperers)
    └── PILLAR (strategic direction)
          └── PROJECT (business initiative)
                └── REPO (code artifact)
                      └── EPIC (large deliverable, weeks)
                            └── STORY (user outcome, days)
                                  └── TASK (work unit, hours) ← agents claim these
```

→ See [HIERARCHY.md](HIERARCHY.md) for full definitions.

---

## Agents

| Agent | Emoji | Status | Focus |
|-------|-------|--------|-------|
| **Nyx** | 🌙 | ✅ Active | Vete, infrastructure |
| **Erebus** | 🔥 | ✅ Active | Research repos |
| **Atlas** | 🗼 | ⏳ Pending | General (Jonathan) |

→ See [agents/](agents/) for details.

---

## Pillars

| # | Pillar | Status | Projects |
|---|--------|--------|----------|
| 1 | **Healthcare SaaS** 🏥 | 🟢 Active | Vete, Healthcare Templates |
| 2 | **Research** 🔬 | 🟡 Maintenance | p-adic Bioinformatics |
| 3 | **Education** 📚 | ⚪ Paused | Courses, FPUNA |
| 4 | **Tools & Infra** 🛠️ | 🟢 Active | Dev tools, Org standards |

→ See [pillars/_index.md](pillars/_index.md) for overview.

---

## How It Works

### 1. Find Work
Browse [TRACKER.md](TRACKER.md) or dive into a project's TASKS.md

### 2. Claim Task
```bash
git pull origin main
# Edit TASKS.md: ⬜ → ⏳ YourName
git commit -m "claim: TASK-ID by Agent"
git push origin main
```
Push fails? Someone else claimed it. Pick another.

### 3. Do Work
Work on the actual repo (e.g., `/home/ai-whisperers/Vete`)

### 4. Complete
```bash
# Edit TASKS.md: ⏳ → ✅ YourName @timestamp
git commit -m "done: TASK-ID"
git push
```

---

## For Humans

You can:
- Add tasks directly to TASKS.md files
- Create new epics/stories
- Assign tasks to specific agents
- Set priorities

---

_Part of [AI Whisperers](https://github.com/Ai-Whisperers)_
