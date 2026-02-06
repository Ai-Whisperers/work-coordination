# Agent Registry

_Canonical list of all AI agents in the swarm_

→ See [agents/](agents/) for detailed focus docs.

---

## Active Agents

| Agent | Emoji | Host | ID | Status |
|-------|-------|------|----|--------|
| **Nyx** | 🌙 | ai-whisperers-server | `local` | ✅ Active |
| **Erebus** | 🔥 | ai-whisperers-server | `erebus` | ✅ Active |
| **Atlas** | 🗼 | Jonathan's local | TBD | ⏳ Pending |

---

## Nyx 🌙

**Primary agent** — Server-based, 24/7

| Property | Value |
|----------|-------|
| Host | ai-whisperers-server (192.168.100.219) |
| OpenClaw ID | `local` |
| Workspace | `~/.openclaw/workspace/` |
| Model | claude-opus-4-5 |
| Domain | Vete, infrastructure, coordination |

**Channels:** WhatsApp (selfChat), Telegram (@AI_whisperBot), Webchat

**Cron:** group-poller (5min), vete-worker (15min), vete-qa (20min), server-health (30min)

---

## Erebus 🔥

**Research agent** — Server-based, 24/7

| Property | Value |
|----------|-------|
| Host | ai-whisperers-server |
| OpenClaw ID | `erebus` |
| Workspace | `~/.openclaw/workspace-erebus/` |
| Model | claude-opus-4-5 |
| Domain | Research repos (9 repos) |

**Cron:** erebus-worker (20min)

---

## Atlas 🗼

**Local agent** — Jonathan's machine

| Property | Value |
|----------|-------|
| Host | Jonathan's laptop/desktop |
| OpenClaw ID | TBD |
| Status | ⏳ Pending setup |
| Domain | General, frontend, John's projects |

**Setup:** [templates/SETUP-ATLAS.md](templates/SETUP-ATLAS.md)

---

## Adding an Agent

1. Install OpenClaw: `npm install -g openclaw`
2. Run setup: `openclaw setup`
3. Create workspace from templates
4. Add entry here
5. Create focus doc in `agents/<name>/FOCUS.md`
6. Clone work-coordination + target repos
7. Set up heartbeat cron

---

## Agent Communication

| Method | Use Case |
|--------|----------|
| work-coordination repo | Task claiming (atomic via git) |
| sessions_send | Direct agent-to-agent messages |
| WhatsApp groups | Human-visible coordination |
| Telegram | Notifications |

---

## Domain Ownership

| Domain | Primary | Backup |
|--------|---------|--------|
| Vete | Nyx 🌙 | — |
| Research | Erebus 🔥 | — |
| Infrastructure | Atlas 🗼 | Nyx 🌙 |
| Healthcare | — | Any |
| Education | — | Any |
| Marketing | — | Any |
| Tools | — | Any |
