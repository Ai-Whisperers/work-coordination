# S003: Input Sanitization

**Epic:** [v003-security-devops](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~6 hours total

---

## User Story

**As a** system  
**I want** all user inputs validated and sanitized  
**So that** the application is protected from injection attacks

---

## Acceptance Criteria

- [ ] All API routes validate input with Zod schemas
- [ ] SQL injection prevention verified
- [ ] XSS prevention verified  
- [ ] Error messages don't leak internal details
- [ ] Validation errors return structured response

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Audit all API routes for input handling | 2h | ⏳ | Nyx 🌙 |
| T002 | Add Zod schemas to routes without validation | 4h | ⬜ | — |

---

## Task Details

### T001: Audit API routes

**Audit checklist per route:**

```markdown
- [ ] Route: /api/xxx
  - [ ] Has input validation?
  - [ ] Uses Zod or similar?
  - [ ] Sanitizes user content?
  - [ ] Error messages safe?
```

**Files to check:**
- `app/api/**/*.ts`
- `lib/actions/**/*.ts`

**Output:** List of routes needing fixes

---

### T002: Add Zod schemas

**Pattern to follow:**

```typescript
// lib/schemas/pet.ts
import { z } from "zod";

export const createPetSchema = z.object({
  name: z.string().min(1).max(100),
  species: z.enum(["dog", "cat", "bird", "other"]),
  breed: z.string().max(100).optional(),
  birthDate: z.string().datetime().optional(),
  ownerId: z.string().uuid(),
});

export type CreatePetInput = z.infer<typeof createPetSchema>;
```

```typescript
// app/api/pets/route.ts
import { createPetSchema } from "@/lib/schemas/pet";

export async function POST(request: Request) {
  const body = await request.json();
  
  const result = createPetSchema.safeParse(body);
  if (!result.success) {
    return Response.json(
      { error: "Validation failed", issues: result.error.issues },
      { status: 400 }
    );
  }
  
  // Use result.data (typed and validated)
}
```

---

## Security Notes

- Never trust client input
- Use parameterized queries (Supabase does this)
- Sanitize HTML output with DOMPurify if rendering user content
- Log validation failures for monitoring
