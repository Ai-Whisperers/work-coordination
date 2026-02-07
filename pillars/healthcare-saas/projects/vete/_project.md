# Project: Vete

**Pillar:** [Healthcare SaaS](../../PILLAR.md)  
**Status:** 🟢 Active  
**Repo:** [Ai-Whisperers/Vete](https://github.com/Ai-Whisperers/Vete)

---

## Overview

Multi-tenant SaaS platform for veterinary clinics in Latin America. Provides clinic management, patient records, appointments, inventory, billing, and a pet owner portal.

**Target Market:** Paraguay (Spanish UI)  
**Production URL:** http://34.151.201.27

---

## Quick Stats

| Metric | Value |
|--------|-------|
| Codebase | 2,851 TypeScript files |
| Lines of Code | 652,493 |
| API Routes | 312 |
| Tests | 1,626 passing |
| Dependencies | 100 |

---

## Current Status

### Revenue
| Metric | Current | Target (Feb) |
|--------|---------|--------------|
| MRR | $0 | $50 |
| Paying Clinics | 0 | 1 |

### Technical Health
| Check | Status |
|-------|--------|
| Tests | ✅ 1,626 passing |
| Build | ✅ Passes |
| Lint | ⚠️ 30 errors, 110 warnings |
| Security | ✅ Hardened (RLS, rate limiting, Zod) |

---

## Epics

| Epic | Status | Progress | Priority |
|------|--------|----------|----------|
| [v003-security-devops](epics/v003-security-devops/_epic.md) | ⏳ Active | 11/12 | High |
| [v004-code-quality](epics/v004-code-quality/_epic.md) | 📋 Ready | 0/16 | Medium |
| [v005-go-to-market](epics/v005-go-to-market/_epic.md) | 📋 Ready | 0/6 | 🔴 CRITICAL |
| [v006-documentation](epics/v006-documentation/_epic.md) | 📋 Ready | 0/4 | Medium |

---

## Features

### Core (Complete ✅)
- Multi-tenant architecture
- Authentication (Supabase)
- Patient/pet management
- Appointments & calendar
- Medical records (SOAP notes)
- Prescriptions with drug dosing
- Vaccinations & schedules
- Invoicing & payments
- Inventory management
- Staff & roles

### Advanced (Complete ✅)
- Laboratory module
- Hospitalization & kennels
- E-commerce with Stripe
- Insurance claims
- Loyalty program
- Analytics dashboards
- WhatsApp integration
- SMS/Email reminders

### In Progress 🔄
- Zod validation (77/312 routes)
- i18n coverage (~80%)

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript (strict) |
| Database | Supabase (PostgreSQL) |
| ORM | Drizzle ORM |
| Auth | Supabase Auth |
| Payments | Stripe |
| SMS | Twilio |
| Email | Resend |
| Testing | Vitest + Playwright |

---

## Team

| Role | Agent/Person |
|------|--------------|
| Lead | Ivan |
| Dev Agent | Nyx 🌙 |
| QA Agent | (cron: vete-qa - disabled) |

---

## Key Decisions

- **Multi-tenant via RLS** - Row-Level Security for data isolation
- **Spanish-first** - Paraguay market, i18n for later expansion
- **Supabase** - Managed PostgreSQL with auth built-in
- **Next.js App Router** - Server components, streaming, API routes

---

## Links

- **Repo:** https://github.com/Ai-Whisperers/Vete
- **Production:** http://34.151.201.27
- **Supabase:** https://app.supabase.com/project/okddppczckbjdotrxiev
- **Docs:** /Vete/web/docs/

---

_Last Updated: 2026-02-06_
