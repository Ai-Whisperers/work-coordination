# S001: CI/CD Pipeline

**Epic:** [v003-security-devops](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~4 hours total

---

## User Story

**As a** developer  
**I want** tests to run automatically on every pull request  
**So that** I catch bugs before they reach the main branch

---

## Acceptance Criteria

- [x] GitHub Actions workflow triggers on push and PR
- [ ] Unit tests run in CI
- [ ] API tests run in CI
- [ ] PR cannot be merged if tests fail
- [ ] Build time < 5 minutes

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Create GitHub Actions workflow file | 2h | ✅ | Nyx 🌙 |
| T002 | Configure Node.js version matrix | 30m | ⬜ | — |
| T003 | Add branch protection rules | 30m | ⬜ | — |

---

## Task Details

### T001: Create GitHub Actions workflow

**File:** `.github/workflows/ci.yml`

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
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
          cache: 'npm'
      - run: npm ci
      - run: npm run test:unit
      - run: npm run test:api
```

**Notes:**
- Cache node_modules for speed
- Run unit tests first (faster feedback)
- Consider parallel jobs later

---

### T002: Configure Node.js version matrix

Test on Node 18 and 20 to ensure compatibility.

---

### T003: Add branch protection rules

GitHub Settings → Branches → Add rule:
- Require status checks to pass
- Require PR reviews (optional for now)

---

## Claiming

```bash
cd /home/ai-whisperers/work-coordination
git pull
# Edit this file: change ⬜ to ⏳ YourName for the task
git commit -m "claim: VETE-V003-S001-T001 by Nyx"
git push
```

---

## Notes

- Start with T001, it unblocks T002 and T003
- If you hit issues with Supabase in CI, check env vars
