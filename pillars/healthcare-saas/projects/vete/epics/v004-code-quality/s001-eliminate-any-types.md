# S001: Eliminate `any` Types

**Epic:** [v004-code-quality](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~5 hours total

---

## User Story

**As a** developer  
**I want** proper TypeScript types everywhere  
**So that** the compiler catches bugs before runtime

---

## Acceptance Criteria

- [ ] `any` count reduced from ~99 to <30
- [ ] No new `any` types introduced
- [ ] All API response types defined
- [ ] Form data properly typed

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Fix `any` in lib/domains/ | 1h | ⬜ | — |
| T002 | Fix `any` in lib/actions/ | 1h | ⬜ | — |
| T003 | Fix `any` in app/api/ routes | 1h | ⬜ | — |
| T004 | Fix `any` in components/ | 1h | ⬜ | — |
| T005 | Create shared type definitions | 1h | ⬜ | — |

---

## Task Details

### T001: Fix `any` in lib/domains/

```bash
cd /home/ai-whisperers/Vete/web
grep -rn ": any" lib/domains/ --include="*.ts"
```

Common fixes:
- Replace `any` with proper interface
- Use `unknown` + type guard if truly unknown
- Import types from Supabase generated types

### T002: Fix `any` in lib/actions/

Server actions often have `any` for form data:
```typescript
// Bad
export async function createPet(data: any) { ... }

// Good
import { CreatePetInput } from '@/lib/schemas/pet';
export async function createPet(data: CreatePetInput) { ... }
```

### T003: Fix `any` in app/api/

API routes need typed request/response:
```typescript
// Bad
export async function POST(req: Request) {
  const body: any = await req.json();
}

// Good
import { CreatePetInput } from '@/lib/schemas/pet';
export async function POST(req: Request) {
  const body = await req.json() as CreatePetInput;
  // Or use Zod validation
}
```

### T004: Fix `any` in components/

Props should be typed:
```typescript
// Bad
function PetCard({ pet }: { pet: any }) { ... }

// Good
import { Pet } from '@/lib/types';
function PetCard({ pet }: { pet: Pet }) { ... }
```

### T005: Create shared type definitions

Create `lib/types/index.ts` with common types:
```typescript
export interface Pet {
  id: string;
  name: string;
  species: string;
  // ...
}

export interface Appointment {
  id: string;
  petId: string;
  // ...
}
```
