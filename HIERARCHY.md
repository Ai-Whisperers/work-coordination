# Work Hierarchy Definition

_How work is organized in AI Whisperers_

---

## Levels (Top → Bottom)

```
COMPANY          Ai-Whisperers (the org)
   │
PILLAR           Strategic direction (3-5 max)
   │
PROJECT          Business initiative with clear outcome
   │
REPO             Code artifact (GitHub repo)
   │
EPIC             Large deliverable (weeks of work)
   │
STORY            User-visible outcome (days of work)
   │
TASK             Single work unit (hours, claimable by agent)
   │
SUBTASK          Optional breakdown of complex tasks
```

---

## Level Definitions

### PILLAR
**What:** A strategic direction for the company. Changes rarely (yearly).
**Count:** 3-5 max
**Owner:** Ivan (human decision)
**Example:** "Healthcare SaaS", "Research & Publications", "Education"

### PROJECT
**What:** A business initiative with a measurable outcome.
**Lifespan:** Months to years
**Owner:** Assigned human or lead agent
**Example:** "Vete Platform", "p-adic Bioinformatics Research", "AI Whisperers Courses"

### REPO
**What:** A GitHub repository (code artifact)
**Relationship:** A project can have 1+ repos. A repo belongs to exactly 1 project.
**Example:** `Vete` repo under "Vete Platform" project

### EPIC
**What:** A large deliverable that takes weeks
**Contains:** Multiple stories
**Example:** "EPIC: API Test Coverage to 80%"

### STORY
**What:** A user-visible outcome
**Format:** "As [who], I want [what], so that [why]"
**Size:** Days of work (1-5 days)
**Example:** "As a dev, I want CI to run tests on PR, so I catch bugs before merge"

### TASK
**What:** A single claimable work unit
**Size:** Hours (1-8 hours)
**Assignable:** Yes — agents claim these
**Example:** "Add GitHub Actions workflow for test run"

### SUBTASK
**What:** Optional breakdown when a task is complex
**Size:** Minutes to hours
**Example:** "Configure Node.js version in workflow"

---

## ID Conventions

| Level | Pattern | Example |
|-------|---------|---------|
| Pillar | `PIL-XXX` | `PIL-001` |
| Project | `PRJ-XXX` | `PRJ-VETE` |
| Repo | GitHub name | `Vete` |
| Epic | `EPIC-XXX` | `EPIC-042` |
| Story | `{REPO}-S-XXX` | `VETE-S-001` |
| Task | `{REPO}-T-XXX` | `VETE-T-042` |
| Subtask | `{TASK}.X` | `VETE-T-042.1` |

---

## State Machine

All items follow the same states:

```
⬜ BACKLOG → 📋 READY → ⏳ IN_PROGRESS → 🔍 REVIEW → ✅ DONE
                              │
                              └── 🔴 BLOCKED (with reason)
```

| State | Meaning |
|-------|---------|
| ⬜ BACKLOG | Identified but not prioritized |
| 📋 READY | Prioritized, can be started |
| ⏳ IN_PROGRESS | Claimed, being worked on |
| 🔍 REVIEW | Work done, needs verification |
| ✅ DONE | Complete and verified |
| 🔴 BLOCKED | Cannot proceed (include reason) |

---

## Rollup Rules

- **Epic progress** = % of stories done
- **Project progress** = % of epics done (weighted by effort)
- **Pillar health** = qualitative (🟢 on track / 🟡 at risk / 🔴 off track)

---

## Relationships

```
PILLAR: Healthcare SaaS
    │
    ├── PROJECT: Vete Platform
    │       ├── REPO: Vete
    │       │     ├── EPIC: Production Readiness
    │       │     │     ├── STORY: CI/CD Pipeline
    │       │     │     │     ├── TASK: Add GH Actions workflow
    │       │     │     │     └── TASK: Configure test matrix
    │       │     │     └── STORY: Security Hardening
    │       │     │           ├── TASK: Add rate limiting
    │       │     │           └── TASK: Input sanitization audit
    │       │     └── EPIC: Feature Complete MVP
    │       │           └── ...
    │       └── REPO: vete-mobile (future)
    │
    ├── PROJECT: Healthcare Templates
    │       ├── REPO: psicologia-ia
    │       ├── REPO: mikie-fisio
    │       └── REPO: Odontology
    │
PILLAR: Research & Publications
    │
    └── PROJECT: p-adic Bioinformatics
            ├── REPO: ternary-vaes-bioinformatics
            ├── REPO: 3-adic-ml
            ├── REPO: ultrametric-antigen-AI
            └── ... (6 more repos)
```

---

## File Structure

```
work-coordination/
├── HIERARCHY.md                 # This file (definitions)
├── TRACKER.md                   # Quick dashboard
├── CLAIMING-PROTOCOL.md         # How to claim tasks
│
├── pillars/
│   ├── _index.md               # All pillars overview
│   │
│   ├── healthcare-saas/
│   │   ├── PILLAR.md           # Pillar definition
│   │   └── projects/
│   │       └── vete/
│   │           ├── _project.md     # Project overview
│   │           ├── _backlog.md     # Unprioritized ideas
│   │           │
│   │           └── epics/
│   │               ├── v001-foundation/
│   │               │   └── _epic.md        # ✅ Complete
│   │               │
│   │               ├── v002-test-coverage/
│   │               │   └── _epic.md        # ✅ Complete
│   │               │
│   │               └── v003-security-devops/   # ⏳ Active
│   │                   ├── _epic.md            # Epic definition
│   │                   ├── s001-cicd-pipeline.md    # Story + tasks
│   │                   ├── s002-rate-limiting.md
│   │                   ├── s003-input-sanitization.md
│   │                   └── s004-auth-hardening.md
│   │
│   ├── research/
│   │   └── ...
│   │
│   └── tools-infra/
│       └── ...
│
├── agents/                      # Agent registry
├── templates/                   # Setup templates
└── archive/                     # Completed/deprecated
```

## Naming Conventions

| Item | Pattern | Example |
|------|---------|---------|
| Project overview | `_project.md` | `vete/_project.md` |
| Backlog | `_backlog.md` | `vete/_backlog.md` |
| Epic folder | `{id}-{slug}/` | `v003-security-devops/` |
| Epic definition | `_epic.md` | `v003-security-devops/_epic.md` |
| Story file | `s{NNN}-{slug}.md` | `s001-cicd-pipeline.md` |

**Underscore prefix (`_`)** = metadata/index file, not a deliverable
