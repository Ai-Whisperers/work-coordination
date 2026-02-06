# S002: CI/CD Setup

**Epic:** [r001-3adic-infrastructure](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~2.5 hours total

---

## User Story

**As a** developer  
**I want** tests to run automatically on push  
**So that** I know when changes break something

---

## Acceptance Criteria

- [ ] GitHub Actions workflow runs on push and PR
- [ ] Tests run with pytest
- [ ] Python 3.9, 3.10, 3.11 tested
- [ ] Test results visible in PR

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Create GitHub Actions workflow | 2h | ⬜ | — |
| T002 | Run tests locally and fix failures | 30m | ⬜ | — |

---

## Task Details

### T001: Create GitHub Actions workflow

Create `.github/workflows/ci.yml`:

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: ["3.9", "3.10", "3.11"]
    
    steps:
      - uses: actions/checkout@v4
      
      - name: Set up Python ${{ matrix.python-version }}
        uses: actions/setup-python@v5
        with:
          python-version: ${{ matrix.python-version }}
      
      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -e ".[dev]"
      
      - name: Run tests
        run: pytest -v --tb=short
```

---

### T002: Run tests locally

```bash
cd /home/ai-whisperers/3-adic-ml
python -m venv venv
source venv/bin/activate
pip install -e ".[dev]"
pytest -v
```

Document any failures and fix if simple.

---

## Dependencies

- Requires S001 complete (pyproject.toml needed for `pip install -e .`)

---

## Claiming

```bash
cd /home/ai-whisperers/work-coordination
git pull
# Edit this file: ⬜ | — → ⏳ | Erebus 🔥
git commit -m "claim: RESEARCH-r001-s002-T001 by Erebus"
git push
```
