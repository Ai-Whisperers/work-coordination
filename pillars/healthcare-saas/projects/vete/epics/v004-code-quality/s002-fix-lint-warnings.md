# S002: Fix Lint Warnings

**Epic:** [v004-code-quality](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~4 hours total

---

## User Story

**As a** developer  
**I want** zero lint warnings  
**So that** the codebase is clean and consistent

---

## Acceptance Criteria

- [ ] `npm run lint` shows 0 warnings
- [ ] No eslint-disable comments (except justified ones)
- [ ] All unused imports removed
- [ ] All unused variables removed

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Fix lint warnings in lib/ | 1h | ⬜ | — |
| T002 | Fix lint warnings in app/ | 1h | ⬜ | — |
| T003 | Fix lint warnings in components/ | 1h | ⬜ | — |
| T004 | Remove unnecessary eslint-disable | 30m | ⬜ | — |

---

## Task Details

### T001: Fix lint warnings in lib/

```bash
cd /home/ai-whisperers/Vete/web
npm run lint -- --fix lib/
# Then manually fix remaining
npm run lint 2>&1 | grep "lib/"
```

Common issues:
- Unused imports: remove them
- Unused variables: prefix with `_` or remove
- Missing deps in useEffect: add them or use eslint-disable with comment

### T002: Fix lint warnings in app/

```bash
npm run lint -- --fix app/
npm run lint 2>&1 | grep "app/"
```

### T003: Fix lint warnings in components/

```bash
npm run lint -- --fix components/
npm run lint 2>&1 | grep "components/"
```

### T004: Remove unnecessary eslint-disable

```bash
grep -rn "eslint-disable" . --include="*.ts" --include="*.tsx" | grep -v node_modules
```

Review each and either:
- Fix the underlying issue
- Add comment explaining why disable is needed
- Remove if no longer needed
