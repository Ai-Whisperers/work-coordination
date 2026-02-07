# Epic m001: Ideas Vault

**Project:** [AI Meetings](../../_project.md)  
**Status:** 📋 Ready  
**Priority:** 🟢 High  
**Target:** Week 1 (Feb 10-14)  
**Effort:** ~5 hours  
**Cost:** $0 (local processing)

---

## Overview

Build a system to transcribe audio recordings (meetings, brainstorms, ideas) and organize them into a searchable knowledge base.

---

## Stories

| ID | Story | Status | Effort |
|----|-------|--------|--------|
| [s001](s001-setup-repo.md) | Set up ideas-vault repo | 📋 Ready | 30m |
| [s002](s002-install-whisper.md) | Install whisper.cpp locally | 📋 Ready | 1h |
| [s003](s003-transcribe-workflow.md) | Create transcribe workflow | 📋 Ready | 2h |
| [s004](s004-summarize-workflow.md) | Create AI summarize workflow | 📋 Ready | 1h |
| [s005](s005-process-backlog.md) | Process existing audio files | 📋 Ready | 30m |

---

## Deliverables

1. **ideas-vault repo** with proper structure
2. **whisper.cpp** installed and working
3. **transcribe.sh** script for batch processing
4. **summarize.sh** script using Claude
5. **Processed backlog** of existing audio files

---

## Technical Design

### Folder Structure
```
ideas-vault/
├── raw/                    # Upload audio files here
│   ├── meetings/
│   ├── brainstorms/
│   └── voice-notes/
├── transcripts/            # Auto-generated
├── summaries/              # Claude summaries
├── topics/                 # Categorized insights
│   ├── product.md
│   ├── marketing.md
│   ├── technical.md
│   └── clients.md
├── action-items/           # Extracted todos
└── scripts/
    ├── transcribe.sh
    ├── summarize.sh
    └── process-all.sh
```

### Workflow
```bash
# 1. Add audio file
cp meeting.m4a ideas-vault/raw/meetings/

# 2. Transcribe
./scripts/transcribe.sh raw/meetings/meeting.m4a

# 3. Summarize + categorize
./scripts/summarize.sh transcripts/meeting.txt

# 4. Or batch process
./scripts/process-all.sh raw/
```

### Whisper.cpp Setup
```bash
# Clone and build
git clone https://github.com/ggerganov/whisper.cpp
cd whisper.cpp
make

# Download model (medium is good balance)
./models/download-ggml-model.sh medium

# Transcribe
./main -m models/ggml-medium.bin -f audio.wav -otxt
```

---

## Success Criteria

- [ ] Can transcribe audio file in <2x real-time
- [ ] Transcripts are accurate (>90%)
- [ ] Summaries capture key points
- [ ] Topics auto-categorized
- [ ] Action items extracted
