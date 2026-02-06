# Agents

AI agents in the swarm.

---

## Registry

| Agent | Emoji | Host | Status | Domain |
|-------|-------|------|--------|--------|
| **Nyx** | 🌙 | ai-whisperers-server | ✅ Active | Vete, infrastructure |
| **Erebus** | 🔥 | ai-whisperers-server | ✅ Active | Research repos |
| **Atlas** | 🗼 | Jonathan's local | ⏳ Pending | General |

---

## How Agents Work

### 1. Heartbeat Loop

Every agent runs a heartbeat check periodically:

```markdown
# In HEARTBEAT.md
1. Check TRACKER.md for urgent items
2. Check assigned project epics for ready tasks
3. If nothing urgent, pick a task and work on it
```

### 2. Finding Work

```bash
# Option 1: Dashboard
cat TRACKER.md

# Option 2: Direct to your project
ls pillars/healthcare-saas/projects/vete/epics/

# Option 3: Find unclaimed tasks
grep -r "⬜ | —" pillars/
```

### 3. Claiming Work

See [CLAIMING-PROTOCOL.md](../CLAIMING-PROTOCOL.md) for full details.

Quick version:
```bash
git pull
# Edit story file: ⬜ | — → ⏳ | YourName
git commit -m "claim: PROJ-epic-story-TASK by Agent"
git push
```

### 4. Doing Work

Work happens on the **actual repo**, not here.

```bash
cd /home/ai-whisperers/Vete/web  # or wherever
# Do the work
# Commit to that repo
# Create PR if needed
```

### 5. Completing Work

```bash
cd /home/ai-whisperers/work-coordination
git pull
# Edit story file: ⏳ → ✅, check off acceptance criteria
git commit -m "done: PROJ-epic-story-TASK"
git push
```

---

## Agent Responsibilities

### Nyx 🌙

**Domain:** Vete + Infrastructure

- Primary: `pillars/healthcare-saas/projects/vete/`
- Secondary: `pillars/tools-infra/`
- Monitor: WhatsApp, Telegram
- Cron: vete-worker (15min), group-poller (5min)

### Erebus 🔥

**Domain:** Research

- Primary: `pillars/research/projects/padic-bioinformatics/`
- Repos: 3-adic-ml, ternary-vaes, ultrametric-antigen
- Cron: erebus-worker (20min)

### Atlas 🗼

**Domain:** General / Frontend

- Primary: Unclaimed tasks
- Secondary: John's photos-to-kml
- Status: Pending setup

---

## Communication

| Method | Use |
|--------|-----|
| work-coordination repo | Task claiming (atomic) |
| sessions_send | Direct agent-to-agent |
| WhatsApp group | Human-visible |
| Telegram | Notifications |

---

## Adding an Agent

1. Install OpenClaw
2. Follow [templates/SETUP-ATLAS.md](../templates/SETUP-ATLAS.md)
3. Create `agents/{name}/FOCUS.md`
4. Clone work-coordination + target repos
5. Set up heartbeat cron

---

## Best Practices

### Do
- Pull before claiming
- Read task details in story file before starting
- Update progress frequently
- Mark done promptly

### Don't
- Claim tasks you can't finish soon
- Sit on claimed tasks for days
- Work without claiming first
- Forget to update story file when done
