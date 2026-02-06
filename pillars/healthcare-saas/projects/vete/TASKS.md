# Vete Tasks

**Project:** [Vete](PROJECT.md)  
**Claim via:** [CLAIMING-PROTOCOL.md](../../../../CLAIMING-PROTOCOL.md)

---

## 🚨 How to Claim

```bash
cd /home/ai-whisperers/work-coordination
git pull origin main
# Edit this file: ⬜ → ⏳ YourName
git commit -m "claim: VETE-T-XXX by AgentName"
git push origin main
```

If push fails, someone else claimed it. Pick another.

---

## Active Tasks

| ID | Task | Story | Effort | Status | Owner |
|----|------|-------|--------|--------|-------|
| — | — | — | — | — | — |

_No tasks currently in progress_

---

## Ready to Claim

### Security & DevOps (EPIC-V003)

| ID | Task | Story | Effort | Status |
|----|------|-------|--------|--------|
| VETE-T-001 | Create GH Actions CI workflow | S-008 | 2h | ⬜ |
| VETE-T-002 | Configure test matrix | S-008 | 1h | ⬜ |
| VETE-T-003 | Add branch protection rules | S-008 | 30m | ⬜ |
| VETE-T-004 | Research rate limiting options | S-009 | 1h | ⬜ |
| VETE-T-005 | Implement rate limiter | S-009 | 3h | ⬜ |
| VETE-T-006 | Audit API input handling | S-010 | 2h | ⬜ |
| VETE-T-007 | Add Zod schemas | S-010 | 4h | ⬜ |
| VETE-T-008 | Review Supabase auth config | S-011 | 1h | ⬜ |
| VETE-T-009 | Add failed login monitoring | S-011 | 2h | ⬜ |

### Code Quality (EPIC-V004)

| ID | Task | Story | Effort | Status |
|----|------|-------|--------|--------|
| VETE-T-010 | Fix `any` types batch 1 | S-012 | 2h | ⬜ |
| VETE-T-011 | Fix `any` types batch 2 | S-012 | 2h | ⬜ |
| VETE-T-012 | Fix lint warnings batch 1 | S-013 | 1h | ⬜ |
| VETE-T-013 | Fix lint warnings batch 2 | S-013 | 1h | ⬜ |

---

## Completed Today

| ID | Task | Owner | Completed |
|----|------|-------|-----------|
| — | — | — | — |

---

## Blocked

| ID | Task | Reason | Unblocked By |
|----|------|--------|--------------|
| — | — | — | — |

---

## Task Stats

| Metric | Count |
|--------|-------|
| Total tasks | 13 |
| Ready | 13 |
| In Progress | 0 |
| Blocked | 0 |
| Done today | 0 |

---

## Notes for Agents

### VETE-T-001: GH Actions workflow
- Use reusable workflow from `.github` if available
- Run both `npm run test:unit` and `npm run test:api`
- Cache node_modules

### VETE-T-005: Rate limiter
- Options: `@upstash/ratelimit`, `next-rate-limit`, custom
- Consider Redis for distributed (future multi-instance)
- Start simple, can upgrade later

### VETE-T-007: Zod schemas
- Check `lib/actions/` for server actions
- Each action should validate input with Zod
- Return typed errors
