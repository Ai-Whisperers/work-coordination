# 🔬 Research Domain — Bioinformatics & p-adic ML

**Owner:** Erebus 🔥

Ivan's computational biology research combining p-adic geometry with machine learning for HIV evolution analysis.

---

## Core Concept

Traditional ML uses real numbers (ℝ). These repos explore **p-adic numbers** (specifically 3-adic) which have ultrametric properties that better model hierarchical/tree-like biological data like genetic sequences.

Key insight: Evolutionary trees are naturally ultrametric → p-adic geometry fits better than Euclidean.

---

## Repository Hierarchy

```
FOUNDATIONAL
    └── 3-adic-ml            ← Core math library
         │
ANALYSIS  
    ├── ternary-engine       ← C++ performance core
    └── tnas-ternary-toolkit ← Differentiable tools
         │
APPLICATION
    ├── ternary-vaes-bioinformatics  ← ★ FLAGSHIP
    │   └── Validated on 4 biological domains
    │
    ├── ultrametric-antigen-AI      ← Antigen analysis
    │   └── Hyperbolic + 3-adic VAE
    │
    └── codon-encoder-*             ← Sequence encoding
         ├── codon-encoder-api
         └── codon-encoder-VIH-focused
                  │
SPECIALIZED
    └── geoprot               ← Protein geometry
```

---

## Active Repositories

### Tier 1 — Active Development

| Repo | Description | Priority |
|------|-------------|----------|
| **[ternary-vaes-bioinformatics](ternary-vaes/)** | Flagship - 1,230x compression | HIGH |
| **[ultrametric-antigen-AI](ultrametric-antigen/)** | Antigen analysis | HIGH |
| **[3-adic-ml](3-adic-ml/)** | Core library | HIGH |

### Tier 2 — Maintenance

| Repo | Description | Status |
|------|-------------|--------|
| ternary-vaes-analysis | Analysis tools | Stable |
| ternary-engine | C++ core | Stable |
| tnas-ternary-toolkit | Toolkit | Stable |

### Tier 3 — Specialized

| Repo | Description | Status |
|------|-------------|--------|
| codon-encoder-api | Encoding API | Stable |
| codon-encoder-VIH-focused | HIV encoder | Stable |
| geoprot | Protein geometry | Stable |

---

## Quick Stats

| Metric | Value |
|--------|-------|
| Total repos | 9 |
| Python files | ~500+ |
| Test coverage | Varies |
| Papers referenced | Multiple |

---

## Getting Started

```bash
# Clone core repos
cd /home/ai-whisperers
git clone https://github.com/Ai-Whisperers/ternary-vaes-bioinformatics.git
git clone https://github.com/Ai-Whisperers/3-adic-ml.git
git clone https://github.com/Ai-Whisperers/ultrametric-antigen-AI.git

# Set up environment
cd ternary-vaes-bioinformatics
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

## Erebus Focus Order

1. **3-adic-ml** — Add LICENSE, pyproject.toml, CI
2. **ternary-vaes-bioinformatics** — Run tests, clear TODOs
3. **ultrametric-antigen-AI** — Document relationship, audit

See individual repo folders for detailed tasks.
