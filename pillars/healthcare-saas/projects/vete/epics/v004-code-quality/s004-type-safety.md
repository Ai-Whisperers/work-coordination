# S004: Type Safety Improvements

**Epic:** [v004-code-quality](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~4 hours total

---

## User Story

**As a** developer  
**I want** stronger type safety  
**So that** TypeScript prevents more bugs

---

## Acceptance Criteria

- [ ] Strict null checks pass
- [ ] No type assertions without validation
- [ ] Supabase types generated and used
- [ ] Form schemas match API types

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Regenerate Supabase types | 30m | ⬜ | — |
| T002 | Fix null/undefined handling | 1h | ⬜ | — |
| T003 | Add Zod schemas for all forms | 1.5h | ⬜ | — |
| T004 | Remove unsafe type assertions | 1h | ⬜ | — |

---

## Task Details

### T001: Regenerate Supabase types

```bash
cd /home/ai-whisperers/Vete/web
npx supabase gen types typescript --project-id okddppczckbjdotrxiev > lib/database.types.ts
```

### T002: Fix null/undefined handling

Find potential null issues:
```bash
grep -rn "!" lib/ app/ --include="*.ts" --include="*.tsx" | grep -v "!=" | grep -v "!==" | head -20
```

Replace non-null assertions with proper checks:
```typescript
// Bad
const name = user!.name;

// Good
const name = user?.name ?? 'Unknown';
// Or throw if required
if (!user) throw new Error('User required');
```

### T003: Add Zod schemas for all forms

Each form should have a schema:
```typescript
// lib/schemas/pet.ts
import { z } from 'zod';

export const petSchema = z.object({
  name: z.string().min(1, 'Name required'),
  species: z.enum(['dog', 'cat', 'bird', 'other']),
  breed: z.string().optional(),
});

export type PetInput = z.infer<typeof petSchema>;
```

### T004: Remove unsafe type assertions

Find `as` casts:
```bash
grep -rn " as " lib/ app/ --include="*.ts" --include="*.tsx" | head -20
```

Replace with:
- Proper type inference
- Type guards
- Zod validation
