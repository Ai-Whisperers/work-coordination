# EPIC-V004: Code Quality

**Status:** 📋 Ready  
**Owner:** Nyx 🌙  
**Target:** 2026-02-15

---

## Goal

Clean up technical debt, improve type safety, and reduce warnings.

---

## Metrics

| Metric | Current | Target |
|--------|---------|--------|
| `any` types | ~99 | <30 |
| Lint warnings | ~96 | 0 |
| Console.log | ~20 | 0 |
| Type suppressions | ~17 | <5 |

---

## Stories

| ID | Story | Status | Tasks |
|----|-------|--------|-------|
| [s001](s001-eliminate-any-types.md) | Eliminate `any` types | 📋 Ready | 5 |
| [s002](s002-fix-lint-warnings.md) | Fix lint warnings | 📋 Ready | 4 |
| [s003](s003-console-cleanup.md) | Console statement cleanup | 📋 Ready | 3 |
| [s004](s004-type-safety.md) | Type safety improvements | 📋 Ready | 4 |

---

## Acceptance Criteria

- [ ] `any` count < 30
- [ ] Zero lint warnings
- [ ] No console.log in production code
- [ ] Type suppressions < 5

---

## Progress

```
[                    ] 0% (0/16 tasks)
```
