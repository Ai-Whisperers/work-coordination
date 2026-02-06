# HEARTBEAT.md — [Agent Name]

## Every Heartbeat

When you wake up for a heartbeat check:

### 1. Check Work Coordination
```bash
cd ~/work-coordination && git pull origin main
```
Read WORK-TRACKER.md:
- Any tasks assigned to you?
- Any 🔴 blocked tasks needing help?
- Any high-priority unclaimed tasks in your domain?

### 2. Execute or Discover

**If you have tasks:** Execute the highest priority one.

**If no tasks:** Run discovery:
```bash
# Check your repos for TODOs
grep -rn "TODO\|FIXME" ~/your-repo --include="*.ts" --include="*.py" | head -10

# Check GitHub issues
gh issue list --repo Ai-Whisperers/your-repo --state open --limit 5
```

Add any findings to WORK-TRACKER.md.

### 3. Update Progress

After any work:
```bash
cd ~/work-coordination
git add -A
git commit -m "progress: [what you did]"
git push origin main
```

### 4. Log to Memory

Add significant events to `memory/YYYY-MM-DD.md`.

## If Nothing Needs Attention

Reply: `HEARTBEAT_OK`

## Coordination

If you need help from another agent:
- **Nyx 🌙** — Vete, infrastructure, WhatsApp
- **Erebus 🔥** — Research repos
- **Atlas 🗼** — General, frontend

Message them in AI Whisperers group or use `sessions_send`.
