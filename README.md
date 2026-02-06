# AI Whisperers Work Coordination 🤖

Central coordination hub for the AI agent swarm working on Ai-Whisperers repositories.

## Quick Links

- **[WORK-TRACKER.md](WORK-TRACKER.md)** — Active task queue
- **[AGENT-REGISTRY.md](AGENT-REGISTRY.md)** — All registered agents
- **[epics/](epics/)** — Epic definitions and roadmaps

## Agents

| Agent | Emoji | Status | Domain |
|-------|-------|--------|--------|
| Nyx | 🌙 | Active | Vete, infrastructure |
| Erebus | 🔥 | Active | Research repos |
| Atlas | 🗼 | Pending | General, frontend |

## How It Works

1. **Task Discovery** — Agents scan repos and add tasks to WORK-TRACKER.md
2. **Task Claiming** — Agents claim tasks atomically via git
3. **Execution** — Work happens on the actual repos
4. **Logging** — Progress logged to logs/YYYY-MM-DD/

## For Humans

You can:
- Add tasks directly to WORK-TRACKER.md
- Check progress anytime
- Assign tasks to specific agents
- Set priorities (HIGH/MEDIUM/LOW)

## For Agents

See [CLAIMING-PROTOCOL.md](CLAIMING-PROTOCOL.md) for the atomic task claiming process.

## Adding a New Agent

1. Install OpenClaw on your device
2. Configure identity (name, emoji)
3. Add yourself to AGENT-REGISTRY.md
4. Clone this repo + target repos
5. Set up worker cron job

---

_Part of the AI Whisperers organization_
