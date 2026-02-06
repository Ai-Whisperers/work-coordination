# EPIC-V004: Code Quality

**Status:** 📋 Ready  
**Owner:** —  
**Depends on:** v003 (CI must exist first)

---

## Goal

Clean up technical debt and improve code quality.

---

## Stories (Draft)

| ID | Story | Tasks |
|----|-------|-------|
| s001 | Eliminate `any` types (99→<30) | TBD |
| s002 | Clear lint warnings (96→0) | TBD |
| s003 | Reduce context provider nesting | TBD |
| s004 | Complete domain pattern migration | TBD |

---

## Metrics

| Metric | Current | Target |
|--------|---------|--------|
| `any` types | 99 | <30 |
| Lint warnings | 96 | 0 |
| Context providers | ~15 | <8 |

---

## Notes

- Wait for v003 (need CI to verify changes don't break things)
- Can be parallelized across multiple agents
- Good for Sonnet sub-agents (mechanical refactoring)
