# PRJ-PBIO: p-adic Bioinformatics

**Pillar:** [Research & Publications](../../PILLAR.md)  
**Status:** 🟡 Maintenance  
**Owner:** Erebus 🔥

---

## Overview

Computational biology research using p-adic (3-adic) geometry for HIV evolution analysis.

---

## Repository Hierarchy

```
FOUNDATIONAL (start here)
    └── 3-adic-ml              ← Core math library

ANALYSIS TOOLS
    ├── ternary-engine         ← C++ performance
    └── tnas-ternary-toolkit   ← Differentiable tools

APPLICATION (main work)
    ├── ternary-vaes-bioinformatics  ← ★ FLAGSHIP
    ├── ultrametric-antigen-AI       ← Antigen analysis
    └── codon-encoder-*              ← Sequence encoding

SPECIALIZED
    └── geoprot                ← Protein geometry
```

---

## Repositories

| Repo | Description | Files | Tests | CI | License |
|------|-------------|-------|-------|----|---------| 
| **ternary-vaes-bioinformatics** | Flagship | 251 | 38 | ✅ | ✅ |
| **3-adic-ml** | Core library | 30 | 7 | ❌ | ❌ |
| **ultrametric-antigen-AI** | Antigen | 251 | 38 | ✅ | ✅ |
| ternary-vaes-analysis | Analysis | — | — | — | — |
| ternary-engine | C++ core | — | — | — | — |
| tnas-ternary-toolkit | Toolkit | — | — | — | — |
| codon-encoder-api | Codon API | — | — | — | — |
| codon-encoder-VIH-focused | HIV encoder | — | — | — | — |
| geoprot | Protein geo | — | — | — | — |

---

## Epics

| ID | Epic | Status | Progress |
|----|------|--------|----------|
| EPIC-R001 | 3-adic-ml Infrastructure | 📋 Ready | 0% |
| EPIC-R002 | ternary-vaes Testing | 📋 Ready | 0% |
| EPIC-R003 | Documentation | ⬜ Backlog | 0% |
| EPIC-R004 | Paper Draft | ⬜ Backlog | 0% |

---

## EPIC-R001: 3-adic-ml Infrastructure

**Goal:** Make 3-adic-ml production-ready

| Story | Tasks | Status |
|-------|-------|--------|
| Add LICENSE (MIT) | 1 | ⬜ |
| Create pyproject.toml | 1 | ⬜ |
| Set up GitHub Actions CI | 2 | ⬜ |
| Run and document tests | 1 | ⬜ |

---

## EPIC-R002: ternary-vaes Testing

**Goal:** Verify flagship repo is working

| Story | Tasks | Status |
|-------|-------|--------|
| Run full test suite | 1 | ⬜ |
| Fix any failures | ? | ⬜ |
| Clear 2 TODOs | 2 | ⬜ |
| Add .env.example | 1 | ⬜ |

---

## Cloning

```bash
cd /home/ai-whisperers
git clone https://github.com/Ai-Whisperers/3-adic-ml.git
git clone https://github.com/Ai-Whisperers/ternary-vaes-bioinformatics.git
git clone https://github.com/Ai-Whisperers/ultrametric-antigen-AI.git
```

---

## Local Paths

All repos should be in `/home/ai-whisperers/`:
- `/home/ai-whisperers/3-adic-ml`
- `/home/ai-whisperers/ternary-vaes-bioinformatics`
- `/home/ai-whisperers/ultrametric-antigen-AI`
