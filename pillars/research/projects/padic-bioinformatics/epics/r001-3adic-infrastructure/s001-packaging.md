# Story s001: Package Structure

**Epic:** [r001-3adic-infrastructure](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 3 hours

## User Story
As a researcher, I want proper Python packaging so the library can be installed via pip.

## Acceptance Criteria
- [ ] MIT LICENSE file
- [ ] pyproject.toml with metadata
- [ ] README.md with usage examples
- [ ] Package structure (__init__.py files)
- [ ] Install works: `pip install -e .`

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Add MIT LICENSE file | 15m | ⏳ | Erebus 🔥 |
| T002 | Create pyproject.toml | 30m | ⬜ | — |
| T003 | Write README with examples | 45m | ⬜ | — |
| T004 | Add __init__.py files | 20m | ⬜ | — |
| T005 | Test pip install -e . | 20m | ⬜ | — |
| T006 | Add version file | 15m | ⬜ | — |

## Technical Notes
- Target repo: 3-adic-ml
- Use modern pyproject.toml (no setup.py)
- Python >= 3.10
