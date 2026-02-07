# Story s001: Symptom Checker Chatbot

**Epic:** [v009-ai-features](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 8 hours

## User Story
As a pet owner, I want to describe my pet's symptoms and get guidance so I know if I need to visit the vet.

## Acceptance Criteria
- [ ] Chat interface for symptom input
- [ ] AI-powered symptom analysis
- [ ] Urgency level indication (low/medium/high/emergency)
- [ ] Suggested next steps
- [ ] Option to book appointment directly
- [ ] Disclaimer about not replacing vet advice

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Design chat UI component | 1h | ⬜ | — |
| T002 | Create symptom analysis prompt | 1h | ⬜ | — |
| T003 | Implement Claude API integration | 1h | ⬜ | — |
| T004 | Build urgency classification logic | 1h | ⬜ | — |
| T005 | Add species/breed context | 45m | ⬜ | — |
| T006 | Create appointment booking CTA | 45m | ⬜ | — |
| T007 | Add conversation history | 1h | ⬜ | — |
| T008 | Implement disclaimer modal | 30m | ⬜ | — |

## Technical Notes
- Use Claude via OpenRouter
- Store conversations for vet review
- Rate limit: 10 queries/day per user
