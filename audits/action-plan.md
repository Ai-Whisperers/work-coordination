# Repository Action Plan

_What to do with 60 repos_

---

## Immediate Actions (Today)

### 🚨 CRITICAL: Security

| Action | Repo | Time |
|--------|------|------|
| Rotate Groq API key | LangAi | 5 min |
| Rotate Langfuse key | LangAi | 5 min |
| Remove creds from code | LangAi | 15 min |
| Add .env.example | LangAi | 5 min |

---

## This Week

### Delete (Empty/Useless)

| Repo | Reason |
|------|--------|
| geoprot | No code |
| organization-template | Empty |
| blueprint-code-once-deploy-everywhere | Empty |
| scrapped-comments | Data storage, not code |

### Archive (Stale but Maybe Useful)

| Repo | Reason |
|------|--------|
| Information-Archive | No purpose clear |
| Summer-courses | Out of season |
| cluster-template | Not using K8s |
| clustering-for-ai-whisperers-* | 3+ months stale |
| outreach-automation | 3+ months stale |
| Comment-Exctractor | Abandoned |
| Company-resarcher | Abandoned |

### Rename (Bad Names)

| Current | Proposed |
|---------|----------|
| Comment-Exctractor | comment-extractor |
| Company-resarcher | company-researcher |
| clustering-for-ai-whisperers-hosting-and-deploys | devops-config |

---

## This Month

### Consolidate Research (10 → 3)

**Keep:**
- ternary-vaes-bioinformatics (flagship)
- 3-adic-ml (foundation)
- ultrametric-antigen-AI (application)

**Merge into flagship:**
- ternary-vaes-analysis → docs/
- tnas-ternary-toolkit → src/toolkit/
- codon-encoder-api → src/encoders/
- codon-encoder-VIH-focused → src/encoders/

**Archive after verification:**
- ternary-engine (verify C++ exists)
- predictive-additive-capacity-control-library

### Consolidate Marketing (12 → 2)

**Keep (if pursuing marketing):**
- marketing-strategy (reference only)
- ai-whisperers-portfolio-website (update with Vete)

**Archive everything else:**
- All 10 other marketing repos

### Consolidate Education (4 → 1)

**Create:** `ai-whisperers-courses`
- Merge Courses-Content
- Merge courses-projects-examples
- Archive Summer-courses
- Pause courses-website

### Consolidate Feedback (3 → 1)

**Create:** `feedback-platform` or archive all
- customer-feedback-app
- feedbackLens
- feedbackScope-backend

---

## Org-Wide Standards

### Every Repo Must Have

- [ ] README.md with description
- [ ] LICENSE (MIT for public)
- [ ] .gitignore
- [ ] .env.example (if uses env vars)

### Active Repos Must Have

- [ ] CI workflow
- [ ] Tests
- [ ] CONTRIBUTING.md

### Add to .github

- [ ] PR template
- [ ] Issue templates
- [ ] Reusable Node.js CI workflow
- [ ] Reusable Python CI workflow
- [ ] CODEOWNERS file

---

## Focus Areas

### Priority 1: Revenue (Vete)
All effort on making Vete generate revenue.
- Complete v003 security tasks
- Add payment integration
- Get first paying customer

### Priority 2: Cleanup (This Doc)
Reduce from 60 repos to ~20 meaningful ones.
- Delete empties
- Archive stale
- Consolidate duplicates

### Priority 3: Foundation
Set up org standards.
- .github templates
- Reusable workflows
- Documentation standards

---

## Target State

### From 60 repos to:

**Active (5)**
- Vete
- work-coordination
- .github
- photos-to-kml
- work-hours-automated-reports

**Research (3)**
- ternary-vaes-bioinformatics
- 3-adic-ml
- ultrametric-antigen-AI

**Templates (2)**
- psicologia-ia
- ai-whisperers-courses

**Client Work (3)**
- Taller_Ocampos
- mikie-fisio
- folyo

**Private (varies)**
- sarah-* (therapy docs)
- legal
- team-tasks

**Archived (40+)**
- Everything else

---

## Success Metrics

| Metric | Current | Target |
|--------|---------|--------|
| Active repos | 12 | 10 |
| Stale repos | 35 | 0 |
| Dead repos | 13 | 0 (archived) |
| With CI | 5 | All active |
| With tests | 3 | All active |
| Security issues | 1 | 0 |
| **Cognitive load** | HIGH | LOW |

---

_"Simplicity is the ultimate sophistication."_ — Leonardo da Vinci, not about Git repos but it applies
