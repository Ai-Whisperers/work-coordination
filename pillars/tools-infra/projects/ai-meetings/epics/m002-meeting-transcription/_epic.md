# Epic m002: Meeting Transcription

**Project:** [AI Meetings](../../_project.md)  
**Status:** 📋 Ready  
**Priority:** 🟡 Medium  
**Target:** Week 2 (Feb 17-21)  
**Effort:** ~3 hours  
**Cost:** $0 (Fathom free tier)

---

## Overview

Set up automatic transcription for all client meetings using free tools.

---

## Stories

| ID | Story | Status | Effort |
|----|-------|--------|--------|
| [s001](s001-fathom-setup.md) | Set up Fathom account | 📋 Ready | 15m |
| [s002](s002-calendar-connect.md) | Connect to Google Calendar | 📋 Ready | 15m |
| [s003](s003-test-meeting.md) | Test with a real meeting | 📋 Ready | 1h |
| [s004](s004-vault-sync.md) | Sync transcripts to ideas-vault | 📋 Ready | 1h |

---

## Tool: Fathom

**Why Fathom:**
- 100% free, no limits
- Auto-joins Zoom/Meet
- Real-time transcription
- AI summaries + action items
- Clips and highlights

**Setup:**
1. Sign up at fathom.video
2. Install Chrome extension
3. Connect Google Calendar
4. Done — auto-joins all meetings

---

## Alternative: tl;dv

If Fathom doesn't work:
- Similar features
- Free tier available
- Good for Zoom/Meet

---

## Integration with OpenClaw

```bash
# Fathom webhook → OpenClaw
# On meeting end:
# 1. Fathom sends transcript
# 2. OpenClaw saves to ideas-vault
# 3. Claude summarizes
# 4. Categorize and extract actions
```

---

## Success Criteria

- [ ] Meetings auto-transcribed
- [ ] Summaries generated
- [ ] Action items extracted
- [ ] Synced to ideas-vault
