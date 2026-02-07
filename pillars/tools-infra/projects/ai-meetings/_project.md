# Project: AI Meetings & Ideas Vault

**Pillar:** [Tools & Infrastructure](../../PILLAR.md)  
**Status:** 📋 Planning  
**Priority:** 🟡 Medium-High

---

## Overview

Build an integrated system for:
1. **Client Meetings** — Professional video calls with AI transcription
2. **AI Participant** — AI that can talk in meetings (future)
3. **Ideas Vault** — Transcribe & organize brainstorm recordings

---

## Research Summary

### 1. Meeting Platforms for Clients

| Platform | Free Tier | Pricing | Pros | Cons | OpenClaw Integration |
|----------|-----------|---------|------|------|---------------------|
| **Google Meet** | 60 min | Free (Workspace) | Already have it, clients know it | Basic AI features | ✅ Calendar via gog skill |
| **Zoom** | 40 min | $16/mo | Industry standard, best AI Companion | Costs money | Webhooks available |
| **Cal.com + Daily.co** | Generous | Free-$12/mo | Self-hosted, API-first | Setup required | ✅ Full API control |
| **Jitsi** | Unlimited | Free | Open source, self-host | Less polished | ✅ Can self-host |

**🏆 Recommendation:** Start with **Google Meet** (free, you have it). Migrate to **Cal.com + Daily.co** for full API control later.

---

### 2. AI Transcription Services

| Service | Pricing | Accuracy | Speed | Best For |
|---------|---------|----------|-------|----------|
| **OpenAI Whisper API** | $0.006/min | Excellent | Fast | General use, we have key |
| **Whisper.cpp (local)** | Free | Excellent | Slower | Privacy, no API costs |
| **Deepgram** | $0.0043/min | Excellent | Real-time | Live transcription |
| **AssemblyAI** | $0.0042/min | Excellent | Fast | Speaker diarization |
| **Fathom** | Free | Good | Real-time | Zoom/Meet auto-join |
| **Fireflies.ai** | Free tier | Good | Real-time | Auto-join + summarize |
| **tl;dv** | Free tier | Good | Real-time | Clips + highlights |

**🏆 Recommendation:** 
- **Batch (Ideas Vault):** Whisper.cpp local (free) or OpenAI Whisper API ($0.006/min)
- **Live Meetings:** Fathom (free) or Deepgram ($0.0043/min for real-time)

---

### 3. AI Meeting Participant (Voice Agent)

| Platform | Pricing | Features | Integration |
|----------|---------|----------|-------------|
| **Vapi.ai** | $0.05/min | Voice AI, custom prompts, phone + web | REST API, webhooks |
| **Recall.ai** | Custom | Bot joins Meet/Zoom, transcribes, can speak | Full meeting API |
| **Bland.ai** | $0.09/min | Phone AI agent, outbound calls | REST API |
| **Retell.ai** | $0.10/min | Low latency voice, custom voices | WebSocket |
| **Play.ht** | $0.04/min | Voice cloning, real-time | REST API |
| **ElevenLabs** | $5/mo+ | Best voice quality, API | ✅ Already have (sag skill) |

**🏆 Recommendation:** 
- **Phase 1:** ElevenLabs for TTS (already have) + Deepgram for STT
- **Phase 2:** Vapi.ai for full voice agent ($0.05/min, reasonable)
- **Future:** Recall.ai for meeting bot that auto-joins

---

### 4. Ideas Vault Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      IDEAS VAULT                             │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────┐    ┌──────────────┐    ┌─────────────┐        │
│  │  INPUT   │    │  TRANSCRIBE  │    │  ANALYZE    │        │
│  │          │    │              │    │             │        │
│  │ - Upload │───▶│ - Whisper    │───▶│ - Claude    │        │
│  │ - Record │    │ - Local/API  │    │ - Summarize │        │
│  │ - Sync   │    │              │    │ - Categorize│        │
│  └──────────┘    └──────────────┘    └─────────────┘        │
│       │                                     │                │
│       │                                     ▼                │
│       │          ┌──────────────────────────────────┐       │
│       │          │           OUTPUT                  │       │
│       │          │                                   │       │
│       │          │  📁 ideas-vault repo              │       │
│       └─────────▶│    ├── transcripts/              │       │
│                  │    ├── summaries/                │       │
│                  │    ├── topics/                   │       │
│                  │    └── action-items/             │       │
│                  └──────────────────────────────────┘       │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Cost Analysis

### Monthly Estimates (Based on Usage)

| Component | Light Use | Medium Use | Heavy Use |
|-----------|-----------|------------|-----------|
| **Google Meet** | Free | Free | Free |
| **Fathom (transcription)** | Free | Free | Free |
| **OpenAI Whisper** (10h) | $3.60 | $7.20 | $18 |
| **Deepgram** (live, 10h) | $2.58 | $5.16 | $13 |
| **ElevenLabs TTS** | $5 | $5 | $22 |
| **Vapi.ai** (1h calls) | $3 | $6 | $15 |
| **Total** | **~$14/mo** | **~$23/mo** | **~$68/mo** |

### Free Tier Maximization

| Service | Free Tier |
|---------|-----------|
| Google Meet | 60 min meetings, unlimited |
| Fathom | Unlimited transcription |
| ElevenLabs | 10k chars/mo |
| Whisper.cpp | Unlimited (local) |
| Cal.com | 1 calendar, unlimited bookings |

**Realistically achievable for $10-20/mo** with smart usage.

---

## OpenClaw Integration Points

### Already Available
- ✅ **gog skill** — Google Calendar integration
- ✅ **openai-whisper-api skill** — Audio transcription
- ✅ **sag skill** — ElevenLabs TTS
- ✅ **exec** — Can run whisper.cpp locally

### To Build
- ⬜ **ideas-vault skill** — Transcribe + categorize workflow
- ⬜ **deepgram skill** — Real-time transcription
- ⬜ **vapi skill** — Voice agent control
- ⬜ **meeting-bot skill** — Join meetings, transcribe, respond

---

## Implementation Phases

### Phase 1: Ideas Vault (Week 1) — FREE
1. Create `ideas-vault` repo with folder structure
2. Set up local Whisper.cpp for transcription
3. Build transcribe → summarize → categorize workflow
4. Process existing audio backlog

**Cost: $0** (local processing)

### Phase 2: Meeting Transcription (Week 2) — FREE
1. Set up Fathom account (free)
2. Connect to Google Calendar
3. Auto-transcribe all client meetings
4. Summaries delivered to ideas-vault

**Cost: $0** (Fathom free tier)

### Phase 3: Enhanced Transcription (Week 3) — ~$5/mo
1. Add Deepgram for real-time (better accuracy)
2. Speaker diarization
3. Keyword detection
4. Integration with OpenClaw cron

**Cost: ~$5/mo** (Deepgram Nova-2)

### Phase 4: Voice AI Agent (Month 2) — ~$20/mo
1. Build Vapi.ai integration
2. AI can answer calls, join meetings
3. Custom voice and personality
4. Hooks into OpenClaw for actions

**Cost: ~$15-25/mo** (Vapi usage-based)

### Phase 5: Full Meeting Bot (Month 3) — ~$50/mo
1. Recall.ai or custom bot
2. Auto-joins meetings
3. Real-time AI participation
4. Takes notes, answers questions, follows up

**Cost: ~$30-50/mo** (Recall.ai)

---

## Quick Wins (This Week)

| Task | Effort | Cost | Impact |
|------|--------|------|--------|
| Create ideas-vault repo | 30m | $0 | Start organizing |
| Install whisper.cpp locally | 1h | $0 | Free transcription |
| Transcribe 5 test audio files | 30m | $0 | Prove workflow |
| Sign up for Fathom | 15m | $0 | Auto-transcribe meetings |
| Connect Fathom to Google Calendar | 15m | $0 | Hands-off transcription |

---

## Technology Stack Decision

| Need | Choice | Why |
|------|--------|-----|
| Meeting Platform | Google Meet → Cal.com | Already have, then upgrade |
| Live Transcription | Fathom (free) → Deepgram | Free first, quality later |
| Batch Transcription | Whisper.cpp local | Free, excellent quality |
| AI Summarization | Claude (via OpenClaw) | Already integrated |
| Voice AI (future) | Vapi.ai | Best price/quality ratio |
| TTS | ElevenLabs | Already configured |

---

## Files to Create

1. `skills/ideas-vault/SKILL.md` — Workflow skill
2. `skills/deepgram/SKILL.md` — Real-time transcription
3. `skills/vapi/SKILL.md` — Voice agent
4. `ideas-vault/` repo — Content storage

---

_Last Updated: 2026-02-06_
