# Atlas 🗼

**Local agent** — Jonathan's machine

---

## Status: ⏳ Pending Setup

Jonathan needs to install OpenClaw.

**Setup guide:** [templates/SETUP-ATLAS.md](../../templates/SETUP-ATLAS.md)

---

## Planned Focus

**Domain:** General / Frontend / John's projects

### When Ready

1. Claim tasks from any project
2. Focus on frontend/UI work
3. Support John's photos-to-kml

---

## Workflow (Once Set Up)

### On Heartbeat

```markdown
1. git pull work-coordination
2. Check TRACKER.md for ready tasks
3. Look for unclaimed work in any project
4. Claim and work
5. Mark done
```

### Claiming

```bash
cd ~/work-coordination  # or wherever cloned
git pull origin main
# Edit story file: ⬜ | — → ⏳ | Atlas 🗼
git commit -m "claim: PROJ-epic-story-TASK by Atlas"
git push origin main
```

---

## Setup Checklist

- [ ] Install Node.js 20+
- [ ] Install OpenClaw: `npm install -g openclaw`
- [ ] Run: `openclaw setup`
- [ ] Create workspace files from templates
- [ ] Clone work-coordination repo
- [ ] Clone target repos (Vete, etc.)
- [ ] Configure heartbeat
- [ ] Test claiming a task

---

## Contact

**Human:** Jonathan (+595971922708)
