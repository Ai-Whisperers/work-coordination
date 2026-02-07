# Story s001: Database Optimization

**Epic:** [v030-performance](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 5 hours

## User Story
As a user, I want fast page loads so I can work efficiently.

## Acceptance Criteria
- [ ] Identify slow queries
- [ ] Add missing indexes
- [ ] Optimize N+1 queries
- [ ] Connection pooling
- [ ] Query caching
- [ ] Monitoring dashboard

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Enable query logging | 20m | ⬜ | — |
| T002 | Analyze slow query log | 45m | ⬜ | — |
| T003 | Add indexes for common queries | 45m | ⬜ | — |
| T004 | Fix N+1 queries with includes | 1h | ⬜ | — |
| T005 | Configure Supabase pooler | 30m | ⬜ | — |
| T006 | Add Redis query cache | 45m | ⬜ | — |
| T007 | Set up pg_stat_statements | 30m | ⬜ | — |
| T008 | Create performance dashboard | 30m | ⬜ | — |

## Technical Notes
- Target: <100ms for common queries
- Index: tenant_id, created_at, status fields
- Cache: list queries, 5 min TTL
