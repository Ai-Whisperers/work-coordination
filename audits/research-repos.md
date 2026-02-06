# Research Repos Deep Dive

_10 repositories for p-adic bioinformatics research_

---

## The Vision

Using **p-adic (3-adic) geometry** to model biological evolution, specifically HIV. The key insight: evolutionary trees are naturally ultrametric, so p-adic numbers are a better fit than real numbers.

**Claimed result:** 1,230x compression (19,683 → 16 dimensions) while preserving biological relationships.

---

## Repository Hierarchy

```
FOUNDATIONAL
    └── 3-adic-ml ★
         │
    └── ternary-engine (C++)
         │
TOOLKIT
    ├── tnas-ternary-toolkit
    └── ternary-vaes-analysis
         │
APPLICATION
    ├── ternary-vaes-bioinformatics ★★★ (FLAGSHIP)
    ├── ultrametric-antigen-AI ★★
    └── codon-encoder-api
         │
SPECIALIZED
    ├── codon-encoder-VIH-focused
    ├── geoprot
    └── predictive-additive-capacity-control-library
```

---

## Individual Assessments

### ternary-vaes-bioinformatics ⭐⭐⭐⭐⭐

**The flagship.** This is where the real work lives.

| Metric | Value |
|--------|-------|
| Files | 251 Python |
| Tests | 38 test files, 2,400+ tests |
| CI | ✅ 3 workflows |
| LICENSE | ✅ MIT |
| README | ✅ Comprehensive |
| Last active | Recent |

**Strengths:**
- Dual-tier architecture (math foundations + bio applications)
- Validated on 4 biological domains
- Proper test coverage

**Weaknesses:**
- 2 TODOs in code (minor)
- Needs .env.example
- Documentation could explain the science better

**Verdict:** Keep, maintain, document.

---

### 3-adic-ml ⭐⭐⭐

**The foundation.** Core math library others depend on.

| Metric | Value |
|--------|-------|
| Files | 30 Python |
| Tests | 7 test files |
| CI | ✅ Just added |
| LICENSE | ✅ Just added |
| pyproject.toml | ✅ Just added |

**Strengths:**
- Clean mathematical primitives
- Essential for other repos

**Weaknesses:**
- Was missing basics until today
- Tests need verification

**Verdict:** Keep, ensure tests pass, document API.

---

### ultrametric-antigen-AI ⭐⭐⭐

**Antigen analysis.** Applies ultrametric geometry to immunology.

| Metric | Value |
|--------|-------|
| Files | 251 Python |
| Tests | 38 test files |
| CI | ✅ |
| LICENSE | ✅ |

**Roast:** Suspiciously similar file count to ternary-vaes-bioinformatics. Are these duplicates? Is one a fork?

**Verdict:** Audit for duplication. Possibly merge or clearly differentiate.

---

### ternary-engine ⭐⭐

**C++ performance core.** When Python isn't fast enough.

| Metric | Value |
|--------|-------|
| Primary language | Python (wrappers?) |
| Last push | Jan 2026 |
| CI | ❌ |

**Roast:** Says C++ but GitHub detects Python. Is the C++ code even there? Performance core that nobody's benchmarked.

**Verdict:** Verify C++ code exists. Add benchmarks or archive.

---

### tnas-ternary-toolkit ⭐⭐

**Differentiable encoder/decoder.** For gradient-based optimization.

| Metric | Value |
|--------|-------|
| Files | Python |
| Last push | Jan 2026 |

**Roast:** "Differentiable" is cool but is anyone differentiating? When was this last used in an experiment?

**Verdict:** If used by flagship, keep. Otherwise, archive.

---

### ternary-vaes-analysis ⭐⭐

**Meta-analysis.** Analyzing the architecture of the VAE system.

| Metric | Value |
|--------|-------|
| Last push | Jan 2026 |

**Roast:** Analysis of analysis. Very academic. Is this a paper draft or actual tooling?

**Verdict:** If it's paper material, move to docs/. Otherwise, archive.

---

### codon-encoder-api ⭐⭐

**Codon encoding API.** Sequence → encoded representation.

| Metric | Value |
|--------|-------|
| Last push | Feb 2026 |
| Language | Python |

**Roast:** Another encoder. How does this differ from codon-encoder-VIH-focused?

**Verdict:** Consolidate with VIH-focused or clearly document difference.

---

### codon-encoder-VIH-focused ⭐

**HIV-focused encoder.** Specialized for HIV sequences.

| Metric | Value |
|--------|-------|
| Last push | Dec 2025 |
| Language | None detected |

**Roast:** No code detected. Is this docs-only? "VIH" is Spanish for HIV — ok for LatAm audience but confusing internationally.

**Verdict:** If empty, delete. If docs, merge into main repo.

---

### geoprot ⭐

**Geometric protein analysis.**

| Metric | Value |
|--------|-------|
| Last push | Jan 2026 |
| Language | None detected |
| README | Exists |

**Roast:** No code. Just a README placeholder. "Geometric protein" sounds cool but there's nothing here.

**Verdict:** DELETE or populate within 1 week.

---

### predictive-additive-capacity-control-library ⭐

**The name is a sentence.**

| Metric | Value |
|--------|-------|
| Last push | Jan 2026 |
| Language | Python |

**Roast:** What does this even do? The description is empty. The name tries to sound impressive but says nothing.

**Verdict:** Document or archive. Nobody knows what this is.

---

## Consolidation Proposal

**Keep (3):**
1. ternary-vaes-bioinformatics (flagship)
2. 3-adic-ml (foundation)
3. ultrametric-antigen-AI (application)

**Merge into flagship (4):**
- ternary-vaes-analysis → docs/analysis/
- codon-encoder-api → src/encoders/
- codon-encoder-VIH-focused → src/encoders/hiv/
- tnas-ternary-toolkit → src/toolkit/

**Verify before archiving (2):**
- ternary-engine (check if C++ actually exists)
- predictive-additive-capacity-control-library (document or delete)

**Delete (1):**
- geoprot (empty)

---

## Action Items

| Priority | Task | Repo |
|----------|------|------|
| HIGH | Check for code duplication | ultrametric vs ternary-vaes |
| HIGH | Delete if empty | geoprot |
| MEDIUM | Add documentation | predictive-* |
| MEDIUM | Verify C++ exists | ternary-engine |
| LOW | Consolidate encoders | codon-encoder-* |
