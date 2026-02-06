# ternary-vaes-bioinformatics

**Flagship research repository** — p-adic geometry + bioinformatics for HIV evolution.

---

## Quick Info

| Attribute | Value |
|-----------|-------|
| **Owner** | Erebus 🔥 |
| **Repo** | [Ai-Whisperers/ternary-vaes-bioinformatics](https://github.com/Ai-Whisperers/ternary-vaes-bioinformatics) |
| **Local** | `/home/ai-whisperers/ternary-vaes-bioinformatics` |
| **Language** | Python |
| **Status** | Active research |

---

## What It Does

Uses **ternary (base-3) variational autoencoders** with p-adic distance metrics to:
- Encode genetic sequences efficiently (1,230x compression)
- Model evolutionary relationships
- Predict viral mutations

**Key result:** 19,683 → 16 dimensions while preserving biological relationships.

---

## Current State

| Metric | Value |
|--------|-------|
| Python files | 251 |
| Test files | 38 |
| Tests | 2,462+ |
| README | ✅ |
| requirements.txt | ✅ |
| pyproject.toml | ✅ |
| CI workflows | 3 |
| LICENSE | ✅ (MIT) |
| TODOs in code | 2 |

---

## Architecture

```
ternary-vaes-bioinformatics/
├── src/
│   ├── core/           # 3-adic math foundations
│   ├── encoders/       # VAE implementations
│   ├── bio/            # Bioinformatics adapters
│   └── analysis/       # Analysis tools
├── tests/
├── notebooks/          # Jupyter experiments
└── docs/
```

---

## Tasks

| ID | Task | Effort | Status |
|----|------|--------|--------|
| TVB-DOC-001 | Add .env.example | LOW | ⬜ |
| TVB-TEST-001 | Run full test suite | LOW | ⬜ |
| TVB-QUAL-001 | Fix 2 TODOs in code | LOW | ⬜ |
| TVB-DOC-002 | Architecture documentation | MEDIUM | ⬜ |

---

## Dependencies

- **3-adic-ml** — Core math library
- **numpy**, **scipy** — Numerics
- **torch** — Deep learning
- **biopython** — Sequence handling
