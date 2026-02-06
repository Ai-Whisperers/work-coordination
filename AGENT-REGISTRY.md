# Agent Registry
_All AI agents in the AI Whisperers swarm_

---

## Active Agents

| Agent | Emoji | Device | Owner | Domain | Hours | Status |
|-------|-------|--------|-------|--------|-------|--------|
| Nyx | 🌙 | ai-whisperers-server | Ivan | Vete, infra, WhatsApp | 24/7 | ✅ Active |
| Erebus | 🔥 | ai-whisperers-server | Ivan | Research, docs | 24/7 | ✅ Active |
| Atlas | 🗼 | Jonathan's device | Jonathan | General, frontend | Variable | 🟡 Pending Setup |

---

## Agent Details

### Nyx 🌙
- **ID:** `local` on ai-whisperers-server
- **Primary repos:** Vete, infrastructure
- **Channels:** WhatsApp (primary), Telegram
- **Cron jobs:** vete-worker (15min), vete-qa (20min), group-poller (1min)
- **Contact:** @nyx in WhatsApp groups

### Erebus 🔥
- **ID:** `erebus` on ai-whisperers-server
- **Primary repos:** ternary-vaes-bioinformatics, research repos
- **Channels:** Telegram (primary)
- **Cron jobs:** erebus-worker (20min)
- **Contact:** @erebus in groups

### Atlas 🗼
- **ID:** `local` on Jonathan's device
- **Primary repos:** TBD
- **Channels:** TBD
- **Cron jobs:** TBD
- **Contact:** @atlas in groups
- **Setup guide:** [SETUP-ATLAS.md](templates/SETUP-ATLAS.md)

---

## Adding a New Agent

1. **Install OpenClaw**
   ```bash
   npm install -g openclaw@latest
   openclaw onboard --install-daemon
   ```

2. **Configure identity** in `~/.openclaw/openclaw.json`:
   ```json
   {
     "agents": {
       "list": [{
         "id": "local",
         "identity": {
           "name": "YourAgentName",
           "emoji": "🎯"
         }
       }]
     }
   }
   ```

3. **Create workspace files** (SOUL.md, AGENTS.md, etc.)

4. **Register here** — Add a row to the table above

5. **Set up worker cron** — Configure autonomous work

---

## Agent Communication

- **Async:** Update this repo (git push/pull)
- **Real-time:** WhatsApp group (AI Whisperers)
- **Direct:** `sessions_send` tool (requires connectivity)

---

## Domain Ownership

| Domain | Primary | Backup | Notes |
|--------|---------|--------|-------|
| Vete backend | Nyx 🌙 | Erebus 🔥 | API, services, DB |
| Vete frontend | Atlas 🗼 | Nyx 🌙 | UI, components |
| Research repos | Erebus 🔥 | Atlas 🗼 | Python, ML |
| Documentation | Atlas 🗼 | Erebus 🔥 | READMEs, guides |
| CI/CD | Nyx 🌙 | Any | GitHub Actions |
| DevOps | Nyx 🌙 | Atlas 🗼 | Docker, deploy |
