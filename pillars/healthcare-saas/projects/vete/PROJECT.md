# PRJ-VETE: Vete Platform

**Pillar:** [Healthcare SaaS](../../PILLAR.md)  
**Status:** 🟢 Active  
**Owner:** Nyx 🌙

---

## Overview

Multi-tenant veterinary clinic management SaaS for Latin America.

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/Vete](https://github.com/Ai-Whisperers/Vete) |
| Local | `/home/ai-whisperers/Vete/web` |
| Production | http://34.151.201.27 |
| Stack | Next.js 15, Supabase, TypeScript |

---

## Product Features

### Core
- 🐕 Pet records & medical history
- 📅 Appointment scheduling
- 📦 Inventory management
- 👥 Staff permissions
- 🏥 Multi-clinic support

### Planned
- 💳 Payment integration
- 📊 Reporting & analytics
- 📱 Mobile app
- 🌐 Multi-language (ES/EN)

---

## Current State

| Metric | Current | Target |
|--------|---------|--------|
| TypeScript files | 2,362 | — |
| Unit tests | 1,626 | 2,000+ |
| API tests | 46% (292/628) | 80%+ |
| Lint warnings | 96 | 0 |
| `any` types | 99 | <30 |
| CI/CD | ❌ | ✅ |
| Paying customers | 0 | 10 |

---

## Work Breakdown

| Doc | Contents |
|-----|----------|
| [EPICS.md](EPICS.md) | All epics for this project |
| [STORIES.md](STORIES.md) | User stories |
| [TASKS.md](TASKS.md) | Claimable tasks |

---

## Epics Overview

| ID | Epic | Status | Progress |
|----|------|--------|----------|
| EPIC-V001 | Foundation (PR #38) | ✅ Done | 100% |
| EPIC-V002 | Test Coverage (PR #39) | ✅ Done | 100% |
| EPIC-V003 | Security & DevOps | ⏳ Active | 0% |
| EPIC-V004 | Code Quality | 📋 Ready | 0% |
| EPIC-V005 | Production Polish | ⬜ Backlog | 0% |
| EPIC-V006 | Feature Complete | ⬜ Backlog | 0% |

---

## Architecture

```
web/
├── app/                    # Next.js App Router
├── components/             # React components
├── lib/
│   ├── domains/           # Domain services
│   │   ├── pets/
│   │   ├── appointments/
│   │   └── ...
│   ├── actions/           # Server actions
│   └── utils/
├── tests/
│   ├── unit/
│   └── api/
└── supabase/              # Migrations
```

---

## Key Technical Decisions

| Decision | Rationale |
|----------|-----------|
| Next.js 15 App Router | Modern React, server components |
| Supabase | PostgreSQL + Auth + RLS, no backend needed |
| Domain service pattern | Testable, maintainable |
| Vitest | Fast, good DX |

---

## Team

| Role | Assignee |
|------|----------|
| Primary dev | Nyx 🌙 |
| Sub-agents | Sonnet workers (cron) |
| Human oversight | Ivan |
