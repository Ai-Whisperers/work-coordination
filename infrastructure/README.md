# 🏗️ Organization Infrastructure

Standards, templates, and CI/CD for all Ai-Whisperers repositories.

---

## Overview

Establish consistent infrastructure across all 50+ repos:
- Issue/PR templates
- CI/CD workflows
- Code standards
- Documentation guidelines

---

## Key Repos

### .github

**Organization community health files**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/.github](https://github.com/Ai-Whisperers/.github) |
| Purpose | Org-wide defaults |

Contains:
- Default issue templates
- Default PR template
- CONTRIBUTING.md
- CODE_OF_CONDUCT.md
- FUNDING.yml

---

### organization-template

**Repository template**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/organization-template](https://github.com/Ai-Whisperers/organization-template) |
| Purpose | New repo starter |

---

### Deployment Blueprints

| Repo | Purpose |
|------|---------|
| blueprint-code-once-deploy-everywhere | Multi-platform deploy |
| deploy-automated-blueprint | Automated deployment |
| cluster-template | K8s configuration |

---

## Standards

### Every Repo Should Have

- [ ] README.md (description, setup, usage)
- [ ] LICENSE (MIT for public)
- [ ] .gitignore
- [ ] .env.example (if env vars used)

### Active Repos Should Also Have

- [ ] CI workflow (.github/workflows/)
- [ ] CONTRIBUTING.md
- [ ] Tests with CI integration

---

## Tasks

| ID | Task | Target | Status |
|----|------|--------|--------|
| ORG-TMPL-001 | Create PR template | .github | ⬜ |
| ORG-TMPL-002 | Create bug issue template | .github | ⬜ |
| ORG-TMPL-003 | Create feature issue template | .github | ⬜ |
| ORG-CI-001 | Reusable Node.js CI workflow | .github | ⬜ |
| ORG-CI-002 | Reusable Python CI workflow | .github | ⬜ |
| ORG-CI-003 | Set up Dependabot for org | .github | ⬜ |

---

## Reusable Workflows

Once created, repos can use:

```yaml
# .github/workflows/ci.yml
name: CI
on: [push, pull_request]
jobs:
  test:
    uses: Ai-Whisperers/.github/.github/workflows/node-ci.yml@main
```

---

## Owner

Shared — Any agent can work on infrastructure.
