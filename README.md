# AI Whisperers Work Coordination 🤖

Central coordination hub for the AI agent swarm working on 50+ Ai-Whisperers repositories.

---

## 📁 Repository Structure

```
work-coordination/
├── WORK-TRACKER.md          # Central task queue
├── CLAIMING-PROTOCOL.md     # How to claim tasks
│
├── domains/                 # Repos grouped by business domain
│   ├── flagship/           # Primary products (Vete)
│   │   └── vete/          # Vete docs, roadmap, tasks
│   ├── research/          # Bioinformatics repos (9)
│   ├── healthcare/        # Practice templates (3)
│   ├── education/         # Courses & training (4)
│   ├── marketing/         # Business development (9)
│   └── tools/             # Utilities (5+)
│
├── infrastructure/         # Org-wide CI/templates
│
├── agents/                 # Agent registry & focus
│   ├── nyx/               # Vete, infrastructure
│   ├── erebus/            # Research repos
│   └── atlas/             # General (pending)
│
├── templates/             # Setup templates
│   └── SETUP-ATLAS.md    # New agent setup guide
│
├── logs/                  # Work logs by date
└── scripts/               # Automation scripts
```

---

## 🤖 Agents

| Agent | Emoji | Status | Domain |
|-------|-------|--------|--------|
| **Nyx** | 🌙 | ✅ Active | Vete, infrastructure |
| **Erebus** | 🔥 | ✅ Active | Research repos |
| **Atlas** | 🗼 | ⏳ Pending | General, frontend |

→ See [agents/](agents/) for details.

---

## 📋 Quick Links

| Document | Purpose |
|----------|---------|
| [WORK-TRACKER.md](WORK-TRACKER.md) | Active task queue |
| [domains/](domains/) | All repos by domain |
| [agents/](agents/) | Agent registry |
| [CLAIMING-PROTOCOL.md](CLAIMING-PROTOCOL.md) | How to claim tasks |

---

## 🎯 Priority Matrix

### 🔴 Critical
- **Vete** — Primary product, revenue path

### 🟠 High
- **LangAi** — Security issue (credential leak)
- **Research repos** — 3-adic-ml, ternary-vaes, ultrametric

### 🟡 Medium
- **Infrastructure** — Org templates, CI
- **photos-to-kml** — John's active project

### 🟢 Low
- **Healthcare templates** — When resources available
- **Marketing repos** — Backlog

---

## 🔄 How It Works

### 1. Task Discovery
Agents scan repos, identify work, add to [WORK-TRACKER.md](WORK-TRACKER.md)

### 2. Task Claiming
```bash
git pull origin main
# Edit WORK-TRACKER.md: ⬜ → ⏳ AgentName
git commit -m "claim: TASK-ID by Agent"
git push origin main
# Push fails? Someone else claimed it. Pick another.
```

### 3. Execution
Work happens on the actual repos, not here.

### 4. Completion
```bash
# Edit WORK-TRACKER.md: ⏳ → ✅ AgentName @TIMESTAMP
git commit -m "done: TASK-ID"
git push
```

→ See [CLAIMING-PROTOCOL.md](CLAIMING-PROTOCOL.md) for full details.

---

## 📊 Stats

| Metric | Count |
|--------|-------|
| Total repos | 50 |
| Active development | ~5 |
| Maintenance | ~15 |
| Private | 22 |

---

## 🆕 Adding an Agent

1. Install OpenClaw on your device
2. Follow [templates/SETUP-ATLAS.md](templates/SETUP-ATLAS.md)
3. Register in [agents/](agents/)
4. Clone this repo + target repos
5. Set up heartbeat/worker cron jobs

---

## 👥 For Humans

You can:
- Add tasks directly to WORK-TRACKER.md
- Check progress anytime
- Assign tasks to specific agents
- Set priorities

---

_Part of the [AI Whisperers](https://github.com/Ai-Whisperers) organization_
