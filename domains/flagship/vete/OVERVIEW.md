# Vete — Veterinary SaaS Platform

**Multi-tenant veterinary clinic management for Latin America.**

---

## Quick Links

- **GitHub:** [Ai-Whisperers/Vete](https://github.com/Ai-Whisperers/Vete)
- **Production:** http://34.151.201.27
- **Local:** `/home/ai-whisperers/Vete/web`

---

## Product Vision

A complete practice management system for veterinary clinics:
- Patient (pet) records & medical history
- Appointment scheduling
- Inventory management
- Staff permissions & multi-clinic support
- Billing & invoicing

**Target market:** Small to medium veterinary clinics in Paraguay and LatAm.

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js 15 (App Router) |
| Styling | Tailwind CSS, shadcn/ui |
| Database | Supabase (PostgreSQL + RLS) |
| Auth | Supabase Auth |
| Language | TypeScript |
| Testing | Vitest (unit + API) |

---

## Current State (2026-02-06)

| Metric | Current | Target |
|--------|---------|--------|
| TypeScript files | 2,362 | — |
| Unit tests passing | 1,626 | 2,000+ |
| API tests passing | 292/628 (46%) | 80%+ |
| Lint warnings | 96 | 0 |
| `any` types | 99 | <30 |
| CI/CD | ❌ | ✅ |
| Production | ✅ GCP | — |

---

## Architecture

```
web/
├── app/                    # Next.js App Router pages
├── components/             # React components
├── lib/
│   ├── domains/           # Domain services (NEW)
│   │   ├── pets/
│   │   ├── appointments/
│   │   ├── inventory/
│   │   └── ...
│   ├── actions/           # Server actions
│   ├── hooks/             # React hooks
│   └── utils/             # Utilities
├── tests/
│   ├── unit/              # Unit tests
│   └── api/               # API route tests
└── supabase/              # DB migrations
```

---

## Key Patterns

### Domain Service Pattern
```typescript
// lib/domains/pets/petService.ts
export const petService = {
  async list(params) { ... },
  async get(id) { ... },
  async create(data) { ... },
  // ...
}
```

### Cleanup Manager (Tests)
```typescript
// tests/helpers/cleanup-manager.ts
CleanupManager.checkpoint('pets');
// ... create test data
CleanupManager.rollbackTo('pets');
```

---

## Development

```bash
cd /home/ai-whisperers/Vete/web
npm install
npm run dev -- -H 0.0.0.0 -p 3000

# Tests
npm run test:unit
npm run test:api
```

---

## Related Docs

- [ROADMAP.md](ROADMAP.md) — Phase breakdown
- [TASKS.md](TASKS.md) — Current task queue
- [Local workplan](/home/ai-whisperers/.openclaw/workspace/vete-workplan.md)
