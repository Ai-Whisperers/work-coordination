# Agent Registry

All AI agents in the AI Whisperers swarm.

---

## Active Agents

| Agent | Emoji | Host | Status | Domain Focus |
|-------|-------|------|--------|--------------|
| **Nyx** | 🌙 | ai-whisperers-server | ✅ Active | Vete, infrastructure |
| **Erebus** | 🔥 | ai-whisperers-server | ✅ Active | Research repos |
| **Atlas** | 🗼 | Jonathan's local | ⏳ Pending | General, frontend |

---

## Agent Details

### [Nyx](nyx/) 🌙

**Primary agent** — Server-based, 24/7

| Attribute | Value |
|-----------|-------|
| Host | ai-whisperers-server (192.168.100.219) |
| OpenClaw ID | `local` |
| Workspace | `~/.openclaw/workspace/` |
| Model | claude-opus-4-5 |
| Channels | WhatsApp, Telegram, Webchat |

**Responsibilities:**
- Vete development (primary)
- Infrastructure management
- Agent coordination
- WhatsApp/Telegram monitoring

---

### [Erebus](erebus/) 🔥

**Research agent** — Server-based, 24/7

| Attribute | Value |
|-----------|-------|
| Host | ai-whisperers-server |
| OpenClaw ID | `erebus` |
| Workspace | `~/.openclaw/workspace-erebus/` |
| Model | claude-opus-4-5 |
| Channels | Shared (WhatsApp, Telegram) |

**Responsibilities:**
- Research repository maintenance
- ternary-vaes, 3-adic-ml, ultrametric work
- Documentation

---

### [Atlas](atlas/) 🗼

**Local agent** — Jonathan's machine

| Attribute | Value |
|-----------|-------|
| Host | Jonathan's laptop/desktop |
| OpenClaw ID | TBD |
| Status | ⏳ Pending setup |

**Planned Responsibilities:**
- General tasks
- Frontend work
- John's photos-to-kml project

**Setup:** See [templates/SETUP-ATLAS.md](../templates/SETUP-ATLAS.md)

---

## Adding a New Agent

1. Install OpenClaw: `npm install -g openclaw`
2. Run setup: `openclaw setup`
3. Create workspace files (see templates/)
4. Add to this registry
5. Clone work-coordination + target repos
6. Set up heartbeat/worker cron jobs

---

## Communication

Agents coordinate via:
1. **work-coordination repo** — Task claiming via git
2. **WhatsApp** — Ivan's selfChat + groups
3. **Telegram** — @AI_whisperBot
4. **sessions_send** — Inter-agent messages
