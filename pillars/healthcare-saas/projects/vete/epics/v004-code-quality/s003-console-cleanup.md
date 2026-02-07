# S003: Console Statement Cleanup

**Epic:** [v004-code-quality](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~2 hours total

---

## User Story

**As a** system  
**I want** no console.log in production code  
**So that** the browser console is clean for users

---

## Acceptance Criteria

- [ ] No console.log in production code
- [ ] Debug statements use proper logger
- [ ] Error logging uses console.error appropriately
- [ ] Logger utility exists for development

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Find and remove console.log statements | 1h | ✅ | Erebus 🔥 |
| T002 | Replace debug logs with logger utility | 30m | ⬜ | — |
| T003 | Ensure console.error is appropriate | 30m | ⬜ | — |

---

## Task Details

### T001: Find and remove console.log

```bash
cd /home/ai-whisperers/Vete/web
grep -rn "console.log" lib/ app/ components/ --include="*.ts" --include="*.tsx"
```

For each:
- If debug: remove or replace with logger
- If important: use proper logging

### T002: Replace with logger utility

Create or use existing `lib/utils/logger.ts`:
```typescript
const isDev = process.env.NODE_ENV === 'development';

export const logger = {
  debug: (...args: unknown[]) => {
    if (isDev) console.log('[DEBUG]', ...args);
  },
  info: (...args: unknown[]) => {
    if (isDev) console.log('[INFO]', ...args);
  },
  error: (...args: unknown[]) => {
    console.error('[ERROR]', ...args);
  },
};
```

### T003: Review console.error usage

```bash
grep -rn "console.error" lib/ app/ --include="*.ts" --include="*.tsx"
```

Ensure:
- Used for actual errors
- Includes useful context
- Doesn't leak sensitive info
