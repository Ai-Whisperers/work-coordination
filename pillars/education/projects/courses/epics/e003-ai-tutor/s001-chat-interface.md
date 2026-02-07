# Story s001: AI Tutor Chat Interface

**Epic:** [e003-ai-tutor](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 6 hours

## User Story
As a student, I want to chat with an AI tutor so I can get help while learning.

## Acceptance Criteria
- [ ] Chat UI component
- [ ] Message history
- [ ] Markdown rendering
- [ ] Code syntax highlighting
- [ ] File/image upload
- [ ] Typing indicators

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Design chat UI layout | 30m | ⬜ | — |
| T002 | Create ChatMessage component | 45m | ⬜ | — |
| T003 | Build ChatInput component | 45m | ⬜ | — |
| T004 | Implement message storage | 45m | ⬜ | — |
| T005 | Add markdown rendering | 30m | ⬜ | — |
| T006 | Integrate code highlighting | 30m | ⬜ | — |
| T007 | Add file upload support | 45m | ⬜ | — |
| T008 | Create typing indicator | 20m | ⬜ | — |
| T009 | Connect to Claude API | 45m | ⬜ | — |

## Technical Notes
- Use react-markdown + rehype-highlight
- Store messages for context
- Course context in system prompt
