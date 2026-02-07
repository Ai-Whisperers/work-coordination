# Story s001: Agent Orchestration

**Epic:** [o004-multi-agent](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 8 hours

## User Story
As a system admin, I want to coordinate multiple agents so they work together effectively.

## Acceptance Criteria
- [ ] Agent registry with capabilities
- [ ] Task queue system
- [ ] Load balancing across agents
- [ ] Agent health monitoring
- [ ] Failover handling
- [ ] Work stealing

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Design agent registry schema | 45m | ⬜ | — |
| T002 | Create agent registration API | 1h | ⬜ | — |
| T003 | Build task queue with Redis | 1h | ⬜ | — |
| T004 | Implement load balancer | 1h | ⬜ | — |
| T005 | Create health check endpoint | 45m | ⬜ | — |
| T006 | Add heartbeat monitoring | 45m | ⬜ | — |
| T007 | Implement failover logic | 1h | ⬜ | — |
| T008 | Add work stealing algorithm | 1h | ⬜ | — |

## Technical Notes
- Use BullMQ for queue
- Agents register capabilities (skills, tools)
- Round-robin with capability matching
