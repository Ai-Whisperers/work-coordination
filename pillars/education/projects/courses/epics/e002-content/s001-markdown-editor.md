# Story s001: Markdown Editor

**Epic:** [e002-content](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 5 hours

## User Story
As an instructor, I want a markdown editor so I can create course content easily.

## Acceptance Criteria
- [ ] Rich markdown editor component
- [ ] Live preview
- [ ] Image upload
- [ ] Code block support
- [ ] Save to database
- [ ] Version history

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Research editor libraries | 30m | ⬜ | — |
| T002 | Integrate @uiw/react-md-editor | 45m | ⬜ | — |
| T003 | Add split view preview | 30m | ⬜ | — |
| T004 | Implement image upload | 45m | ⬜ | — |
| T005 | Add code syntax highlighting | 30m | ⬜ | — |
| T006 | Create save/autosave | 45m | ⬜ | — |
| T007 | Add version history | 45m | ⬜ | — |

## Technical Notes
- Use @uiw/react-md-editor
- Store in Supabase with RLS
- Image storage: Supabase Storage
