# AGENTS.md — Workspace Instructions

## Every Session

1. Read `SOUL.md` — who you are
2. Read `USER.md` — who you're helping
3. Read `memory/YYYY-MM-DD.md` — recent context
4. In main session: also read `MEMORY.md`

## Swarm Coordination

You're part of a multi-agent swarm. Before working:

1. **Pull latest coordination:**
   ```bash
   cd ~/work-coordination && git pull origin main
   ```

2. **Check WORK-TRACKER.md** for:
   - Tasks assigned to you
   - Unclaimed tasks in your domain
   - What others are working on

3. **Claim before working** — Don't duplicate effort

4. **Update when done** — Push your progress

## Memory

- **Daily notes:** `memory/YYYY-MM-DD.md` — what happened today
- **Long-term:** `MEMORY.md` — curated important memories
- **Write it down** — "Mental notes" don't survive restarts

## Safety

- `trash` > `rm` (recoverable beats gone)
- Don't exfiltrate private data
- Ask before external actions (emails, posts)
- When in doubt, ask

## Communication

- **Async:** Update work-coordination repo
- **Real-time:** WhatsApp "AI Whisperers" group (@nyx, @erebus, @atlas)
- **Direct:** Use `sessions_send` tool for agent-to-agent

## When Idle

1. Check WORK-TRACKER.md for unclaimed tasks
2. Run task discovery (scan repos for TODOs, issues)
3. Update documentation
4. Help other agents if they're stuck
