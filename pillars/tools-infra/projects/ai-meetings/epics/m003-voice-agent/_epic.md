# Epic m003: Voice AI Agent

**Project:** [AI Meetings](../../_project.md)  
**Status:** 📋 Future  
**Priority:** 🔵 Low (until m001/m002 done)  
**Target:** Month 2 (March 2026)  
**Effort:** ~15 hours  
**Cost:** ~$20-50/mo

---

## Overview

Build an AI agent that can participate in meetings — listen, understand, and respond with voice.

---

## Stories

| ID | Story | Status | Effort |
|----|-------|--------|--------|
| s001 | Research Vapi.ai vs Retell vs Bland | 📋 Future | 2h |
| s002 | Set up Vapi.ai account | 📋 Future | 1h |
| s003 | Create custom voice persona | 📋 Future | 2h |
| s004 | Build OpenClaw integration | 📋 Future | 4h |
| s005 | Test in real meeting | 📋 Future | 2h |
| s006 | Add to phone line | 📋 Future | 2h |

---

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    VOICE AGENT STACK                     │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐          │
│  │  INPUT   │    │  BRAIN   │    │  OUTPUT  │          │
│  │          │    │          │    │          │          │
│  │ Deepgram │───▶│ Claude   │───▶│ Eleven   │          │
│  │ (STT)    │    │ (LLM)    │    │ Labs     │          │
│  │          │    │          │    │ (TTS)    │          │
│  └──────────┘    └──────────┘    └──────────┘          │
│       │                │                │               │
│       └────────────────┼────────────────┘               │
│                        │                                │
│                        ▼                                │
│              ┌──────────────────┐                       │
│              │     Vapi.ai      │                       │
│              │   Orchestrator   │                       │
│              │                  │                       │
│              │ - Phone numbers  │                       │
│              │ - WebRTC         │                       │
│              │ - Turn-taking    │                       │
│              │ - Interruptions  │                       │
│              └──────────────────┘                       │
│                        │                                │
│                        ▼                                │
│              ┌──────────────────┐                       │
│              │    OpenClaw      │                       │
│              │                  │                       │
│              │ - Context/Memory │                       │
│              │ - Tool access    │                       │
│              │ - Actions        │                       │
│              └──────────────────┘                       │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

---

## Platform Comparison

| Platform | STT | LLM | TTS | Price | Latency | Notes |
|----------|-----|-----|-----|-------|---------|-------|
| **Vapi.ai** | Deepgram | Any | 11Labs/Play.ht | $0.05/min | ~500ms | Best balance |
| **Retell.ai** | Built-in | Any | Built-in | $0.10/min | ~300ms | Lowest latency |
| **Bland.ai** | Built-in | GPT-4 | Built-in | $0.09/min | ~600ms | Best for calls |
| **Play.ai** | Deepgram | Any | Play.ht | $0.04/min | ~800ms | Cheapest |
| **DIY** | Deepgram | Claude | 11Labs | $0.02/min | ~1s+ | Most control |

**🏆 Recommendation:** Start with **Vapi.ai** — best docs, reasonable price, good latency.

---

## Use Cases

1. **Answer phone calls** — AI receptionist for clinic inquiries
2. **Join client meetings** — Take notes, answer questions
3. **Outbound calls** — Follow-up reminders, confirmations
4. **Voice interface** — Talk to OpenClaw hands-free

---

## Vapi.ai Integration

```typescript
// vapi-integration.ts
import Vapi from '@vapi-ai/web';

const vapi = new Vapi('your-api-key');

// Start a call
const call = await vapi.start({
  assistant: {
    model: {
      provider: 'anthropic',
      model: 'claude-sonnet-4-20250514',
    },
    voice: {
      provider: 'elevenlabs',
      voiceId: 'your-voice-id',
    },
    firstMessage: "Hola, soy Nyx de AI Whisperers. ¿En qué puedo ayudarte?",
    context: `You are Nyx, an AI assistant for AI Whisperers.
              You help with veterinary software questions.
              Be helpful, concise, and friendly.
              Speak in Spanish unless asked otherwise.`,
  },
});
```

---

## OpenClaw Skill Design

```markdown
# skills/vapi/SKILL.md

## Commands

- `vapi call <number>` — Initiate outbound call
- `vapi answer` — Answer incoming call
- `vapi join <meeting-url>` — Join video meeting
- `vapi hangup` — End current call
- `vapi status` — Show call status
```

---

## Costs Breakdown

| Component | Per Minute | 10h/month |
|-----------|------------|-----------|
| Vapi platform | $0.02 | $12 |
| Deepgram STT | $0.0043 | $2.58 |
| Claude Sonnet | ~$0.01 | $6 |
| ElevenLabs TTS | $0.01 | $6 |
| **Total** | **$0.05** | **~$27/mo** |

---

## Success Criteria

- [ ] Can make outbound calls
- [ ] Can receive inbound calls
- [ ] Natural conversation flow
- [ ] < 1 second response latency
- [ ] Spanish and English support
- [ ] Integrated with OpenClaw tools
