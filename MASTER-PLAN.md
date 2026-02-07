# AI Whisperers — Master Plan

_Last Updated: 2026-02-06_

---

## 🎯 Mission

Build AI-powered veterinary software (Vete) and supporting infrastructure, using autonomous AI agents for development and operations.

---

## 🏗️ Organization Structure

```
AI Whisperers
├── 🏥 Healthcare SaaS (Pillar 1) ──────────── PRIORITY
│   └── Vete — Veterinary clinic management
│       ├── v003 Security & DevOps ✅ DONE
│       ├── v004 Code Quality ⏳ 16 tasks
│       ├── v005 Go-to-Market 🚨 CRITICAL
│       └── v006 Documentation
│
├── 🔧 Tools & Infrastructure (Pillar 2)
│   ├── OpenClaw — AI agent platform
│   ├── work-coordination — Git-based task management
│   └── AI Meetings — NEW
│       ├── m001 Ideas Vault ⏳
│       ├── m002 Meeting Transcription
│       └── m003 Voice Agent
│
├── 🔬 Research (Pillar 3) — ON HOLD
│   └── ternary-vaes-bioinformatics
│
└── 📚 Education (Pillar 4) — ON HOLD
    └── FPUNA courses
```

---

## 👥 Team

| Agent | Location | Role | Status |
|-------|----------|------|--------|
| **Nyx 🌙** | Server (24/7) | Vete + Infrastructure | ✅ Active |
| **Erebus 🔥** | Server (24/7) | Research repos | ❌ Disabled |
| **Atlas 🗼** | John's local | TBD | ⏳ Pending setup |
| **Ivan** | Human | Founder/Lead | 👤 |

---

## 📊 Current Priorities

### 🚨 P0: Get First Paying Clinic (v005)
**Why:** Technical work means nothing without customers.

| Story | Tasks | Status |
|-------|-------|--------|
| s001 Sales Materials | 5 | 📋 Ready |
| s002 Prospect List | 4 | 📋 Ready |
| s003 Outreach | 4 | 📋 Ready |
| s004 Demo Flow | 3 | 📋 Ready |
| s005 Onboarding | 3 | 📋 Ready |
| s006 Pricing | 3 | 📋 Ready |

### 🟡 P1: AI Meetings & Ideas Vault (m001)
**Why:** Capture brainstorm recordings, improve client meetings.

| Task | Status | Notes |
|------|--------|-------|
| Create ideas-vault folder | ✅ Done | `/home/ai-whisperers/ideas-vault/` |
| Install faster-whisper | ✅ Done | Local, free transcription |
| Download audio from Drive | ⏳ 4/20 files | Ongoing |
| Transcribe backlog | ⏳ Running | 200MB file processing |
| Set up Fathom | 📋 Ready | Free meeting transcription |

### 🟢 P2: Code Quality (v004)
**Why:** Reduce tech debt, improve maintainability.

16 tasks: any types, lint fixes, console cleanup, type safety.

---

## 🔄 How Work Gets Done

### Git-Based Task Coordination

```
work-coordination/
├── TRACKER.md              ← Dashboard (start here)
├── HIERARCHY.md            ← Definitions
├── ACTION-PLAN.md          ← Current focus
└── pillars/
    └── {pillar}/
        └── projects/
            └── {project}/
                └── epics/
                    └── {epic}/
                        └── s001-story.md  ← Task checklist
```

### Claiming a Task

1. **Read TRACKER.md** — Find ready work
2. **Open story file** — Find unclaimed task (⬜)
3. **Edit:** `⬜ | —` → `⏳ | Nyx 🌙`
4. **Commit:** `claim: VETE-v005-s001-T001 by Nyx`
5. **Push** — If push fails, someone else claimed it
6. **Do the work**
7. **Mark done:** `⏳` → `✅`
8. **Commit:** `done: VETE-v005-s001-T001`

### Autonomous Workers (Cron Jobs)

| Job | Interval | Function |
|-----|----------|----------|
| `nyx-worker` | 5 min | Claims & works Vete tasks |
| `group-poller` | 1 min | Polls WhatsApp groups |
| `server-health` | 30 min | Monitors disk/memory/load |

---

## 🎙️ AI Meetings System

### Phase 1: Ideas Vault (Week 1) — $0

**Goal:** Transcribe existing brainstorm recordings.

```bash
# Workflow
1. Audio files → Google Drive folder
2. gog drive download → ideas-vault/raw/
3. faster-whisper → ideas-vault/transcripts/
4. Claude → ideas-vault/summaries/
5. Categorize → ideas-vault/topics/
```

**Infrastructure:**
- `faster-whisper` installed locally (free)
- Scripts in `ideas-vault/scripts/`
- 20+ audio files identified in Drive

### Phase 2: Meeting Transcription (Week 2) — $0

**Goal:** Auto-transcribe all client meetings.

```bash
# Setup
1. Sign up for Fathom (free)
2. Connect to Google Calendar
3. Fathom auto-joins meetings
4. Summaries delivered via email/API
```

### Phase 3: Voice AI Agent (Month 2) — ~$25/mo

**Goal:** AI that talks in meetings.

```bash
# Stack
STT: Deepgram ($0.0043/min)
LLM: Claude (via OpenClaw)
TTS: ElevenLabs (already configured)
Orchestrator: Vapi.ai ($0.05/min total)
```

---

## 📁 Repository Map

### Active (26 repos)

| Repo | Purpose | Priority |
|------|---------|----------|
| **Vete** | Veterinary SaaS | 🚨 P0 |
| **work-coordination** | Task management | 🚨 P0 |
| **ideas-vault** | Brainstorm transcripts | 🟡 P1 |
| ternary-vaes-bioinformatics | Research flagship | 🔵 On hold |

### Local Folders

| Path | Purpose |
|------|---------|
| `~/.openclaw/workspace/` | Agent workspace |
| `~/Vete/` | Main project |
| `~/work-coordination/` | Coordination repo |
| `~/ideas-vault/` | Audio transcripts |
| `~/whisper-venv/` | Transcription env |

---

## 💰 Cost Structure

### Current Monthly (~$15)
- OpenClaw agents: ~$5-10/day (when active)
- ElevenLabs TTS: $5/mo
- Google Suite: Free tier

### With AI Meetings (~$30-50/mo)
- Add Fathom: Free
- Add Deepgram: ~$5/mo (usage-based)
- Add Vapi.ai: ~$15-20/mo (usage-based)

---

## 🗓️ This Week's Focus

### Friday Feb 6 (Today)
- [x] Review autonomous jobs
- [x] Plan AI Meetings system
- [x] Create ideas-vault structure
- [x] Start transcribing audio backlog
- [ ] Complete bio-info transcription
- [ ] Download all audio files from Drive

### Weekend Feb 7-8
- [ ] Process all audio transcripts
- [ ] Create topic summaries
- [ ] Set up Fathom for meetings

### Monday Feb 9
- [ ] Start v005-s001 (Sales Materials)
- [ ] First outreach to vet clinics

---

## 🔗 Key Links

| Resource | URL |
|----------|-----|
| Vete Production | http://34.151.201.27 |
| Work Coordination | github.com/Ai-Whisperers/work-coordination |
| Audio Files | drive.google.com/drive/folders/1-3TKCteCl8eEPEAXvmuN2foGQEtCXOMJ |
| OpenClaw Dashboard | http://127.0.0.1:18789/?token=openclaw-local-2026 |

---

## 📝 Quick Commands

```bash
# Check work status
cd ~/work-coordination && cat TRACKER.md

# Transcribe audio
~/whisper-venv/bin/python3 ~/ideas-vault/scripts/transcribe.py <file.m4a>

# Download from Drive
gog drive download "<file-id>" --out "filename.m4a"

# List Drive folder
gog drive ls --parent "1-3TKCteCl8eEPEAXvmuN2foGQEtCXOMJ"

# Check cron jobs
# (via OpenClaw cron tool)

# Run Vete tests
cd ~/Vete/web && npm run test:unit
```

---

_This document is the single source of truth for AI Whisperers organization._
