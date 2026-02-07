# Story s002: Install Whisper Locally

**Epic:** [m001-ideas-vault](_epic.md)  
**Status:** ✅ Done  
**Effort:** 1 hour

## User Story
As a system admin, I want local transcription so we don't pay per-minute API costs.

## Acceptance Criteria
- [x] faster-whisper installed in venv
- [x] Model downloaded (small)
- [x] Test transcription working
- [ ] GPU acceleration (optional)

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create Python venv | 10m | ✅ | Nyx 🌙 |
| T002 | Install faster-whisper | 20m | ✅ | Nyx 🌙 |
| T003 | Download whisper model | 15m | ✅ | Nyx 🌙 |
| T004 | Test with sample audio | 15m | ✅ | Nyx 🌙 |
| T005 | Enable GPU if available | 30m | ⬜ | — |

## Notes
- Installed at ~/whisper-venv/
- Using small model (good balance)
- CPU-only for now (no GPU)
