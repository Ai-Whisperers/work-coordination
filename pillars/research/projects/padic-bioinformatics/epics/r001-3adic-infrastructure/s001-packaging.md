# S001: Packaging & License

**Epic:** [r001-3adic-infrastructure](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~2 hours total

---

## User Story

**As a** researcher  
**I want** 3-adic-ml to have proper packaging  
**So that** I can install it and understand its license

---

## Acceptance Criteria

- [x] MIT LICENSE file added
- [ ] pyproject.toml created with metadata
- [ ] Package installable via `pip install -e .`
- [ ] README updated with install instructions

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Add MIT LICENSE file | 15m | ✅ | Erebus 🔥 |
| T002 | Create pyproject.toml | 1h | ✅ | Erebus 🔥 |
| T003 | Update README with install instructions | 30m | ⬜ | — |

---

## Task Details

### T001: Add MIT LICENSE file

Create `LICENSE` in repo root:

```
MIT License

Copyright (c) 2024-2026 AI Whisperers

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

### T002: Create pyproject.toml

```toml
[build-system]
requires = ["setuptools>=61.0", "wheel"]
build-backend = "setuptools.build_meta"

[project]
name = "3-adic-ml"
version = "0.1.0"
description = "3-adic machine learning library"
readme = "README.md"
license = {text = "MIT"}
requires-python = ">=3.9"
authors = [
    {name = "AI Whisperers", email = "ivan@aiwhisperers.com"}
]
classifiers = [
    "Development Status :: 3 - Alpha",
    "Intended Audience :: Science/Research",
    "License :: OSI Approved :: MIT License",
    "Programming Language :: Python :: 3",
]
dependencies = [
    "numpy>=1.20",
    "torch>=2.0",
]

[project.optional-dependencies]
dev = ["pytest", "pytest-cov"]

[tool.setuptools.packages.find]
where = ["."]
```

Adjust dependencies based on actual requirements.txt.

---

### T003: Update README

Add installation section:

```markdown
## Installation

```bash
# Clone the repository
git clone https://github.com/Ai-Whisperers/3-adic-ml.git
cd 3-adic-ml

# Install in development mode
pip install -e .

# Or with dev dependencies
pip install -e ".[dev]"
```
```

---

## Claiming

```bash
cd /home/ai-whisperers/work-coordination
git pull
# Edit this file: ⬜ | — → ⏳ | Erebus 🔥
git commit -m "claim: RESEARCH-r001-s001-T001 by Erebus"
git push
```
