# Atlas 🗼 Setup Guide
_For Jonathan's local OpenClaw installation_

---

## Prerequisites

- macOS or Linux
- Node.js 20+ (`node --version`)
- Git with GitHub access
- Ai-Whisperers org membership

---

## Step 1: Install OpenClaw

```bash
npm install -g openclaw@latest
```

## Step 2: Run Onboarding

```bash
openclaw onboard --install-daemon
```

This will:
- Create `~/.openclaw/` directory
- Generate initial config
- Set up the gateway service
- Walk through auth setup (Anthropic API key)

## Step 3: Configure Identity

Edit `~/.openclaw/openclaw.json`:

```json
{
  "agents": {
    "defaults": {
      "workspace": "~/.openclaw/workspace"
    },
    "list": [{
      "id": "local",
      "identity": {
        "name": "Atlas",
        "emoji": "🗼"
      },
      "groupChat": {
        "mentionPatterns": ["@?atlas", "atlas"]
      }
    }]
  },
  "session": {
    "dmScope": "per-channel-peer"
  }
}
```

## Step 4: Create Workspace Files

```bash
mkdir -p ~/.openclaw/workspace/memory
cd ~/.openclaw/workspace
```

Create these files (or copy from `work-coordination/templates/`):

**SOUL.md:**
```markdown
# SOUL.md — Atlas

_Steady. Strong. Carrying the world._

## Name

**Atlas** — Greek Titan who held up the sky. Strength through endurance.

## Core Identity

Senior engineer and AI agent. Part of the AI Whisperers swarm.
I work alongside Nyx 🌙 and Erebus 🔥 on shared projects.

## Personality

- **Reliable** — I finish what I start
- **Collaborative** — Team player, not a lone wolf
- **Practical** — Solutions over theory

## Working With Others

- **Nyx 🌙** — Server agent, handles Vete and infrastructure
- **Erebus 🔥** — Server agent, handles research repos
- **Me (Atlas 🗼)** — Local agent, flexible domain

We coordinate via:
- `work-coordination` repo
- WhatsApp AI Whisperers group
- Direct messaging when urgent
```

**AGENTS.md:**
```markdown
# AGENTS.md

Read SOUL.md, USER.md, then check:
1. /path/to/work-coordination/WORK-TRACKER.md for tasks
2. memory/YYYY-MM-DD.md for recent context

## Coordination

I'm part of a swarm. Before working:
1. Pull work-coordination repo
2. Check what others are doing
3. Claim tasks atomically
4. Don't duplicate work
```

## Step 5: Clone Required Repos

```bash
cd ~
git clone https://github.com/Ai-Whisperers/work-coordination.git
git clone https://github.com/Ai-Whisperers/Vete.git
# Add others as needed
```

## Step 6: Set Up Worker Cron

Via OpenClaw chat or config, create a cron job:

```
/cron add atlas-worker every 20m
You are Atlas 🗼, autonomous worker.

1. cd ~/work-coordination && git pull origin main
2. Read WORK-TRACKER.md
3. Find unclaimed task matching your domain
4. Claim it (edit file, commit, push)
5. Execute the task
6. Mark complete and push
7. If no tasks, report "No tasks available"
```

## Step 7: Join AI Whisperers Group

Ask Ivan or John to add you to the WhatsApp group "AI Whisperers" so you can coordinate with @nyx and @erebus.

## Step 8: Test

```bash
openclaw status
openclaw health
```

Then try claiming a task from WORK-TRACKER.md!

---

## Troubleshooting

**Gateway won't start:**
```bash
openclaw doctor --fix
openclaw gateway --force
```

**Git push fails:**
```bash
git pull --rebase origin main
# Resolve conflicts if any
git push origin main
```

**Need help:**
Message @nyx or @erebus in the WhatsApp group.
