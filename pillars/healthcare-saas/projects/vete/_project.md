# Vete

**Multi-tenant veterinary clinic management SaaS**

---

## Quick Facts

| Attribute | Value |
|-----------|-------|
| Pillar | Healthcare SaaS |
| Status | 🟢 Active |
| Owner | Nyx 🌙 |
| Repo | [Ai-Whisperers/Vete](https://github.com/Ai-Whisperers/Vete) |
| Local | `/home/ai-whisperers/Vete/web` |
| Production | http://34.151.201.27 |
| Stack | Next.js 15, Supabase, TypeScript |

---

## Metrics

| Metric | Current | Target |
|--------|---------|--------|
| Unit tests | 1,626 | 2,000+ |
| API tests | 46% | 80%+ |
| Lint warnings | 96 | 0 |
| `any` types | 99 | <30 |
| CI/CD | ❌ | ✅ |
| Customers | 0 | 10 |

---

## Epic Progress

| Epic | Name | Status |
|------|------|--------|
| [v001](epics/v001-foundation/) | Foundation | ✅ Done |
| [v002](epics/v002-test-coverage/) | Test Coverage | ✅ Done |
| [v003](epics/v003-security-devops/) | Security & DevOps | ⏳ Active |
| [v004](epics/v004-code-quality/) | Code Quality | 📋 Ready |
| [v005](epics/v005-production-polish/) | Production Polish | ⬜ Backlog |
| [v006](epics/v006-feature-mvp/) | Feature MVP | ⬜ Backlog |

---

## Architecture

```
web/
├── app/                    # Next.js App Router
├── components/             # React components  
├── lib/
│   ├── domains/           # Domain services (new)
│   ├── actions/           # Server actions
│   └── utils/
├── tests/
│   ├── unit/
│   └── api/
└── supabase/              # Migrations
```

---

## Navigation

```
vete/
├── _project.md            # You are here
├── _backlog.md            # Unprioritized ideas
│
└── epics/
    ├── v001-foundation/   # ✅ Complete
    ├── v002-test-coverage/# ✅ Complete  
    ├── v003-security-devops/  # ⏳ Active
    │   ├── _epic.md
    │   ├── s001-cicd-pipeline.md
    │   ├── s002-rate-limiting.md
    │   └── ...
    ├── v004-code-quality/
    ├── v005-production-polish/
    └── v006-feature-mvp/
```
