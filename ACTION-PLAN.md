# 🎯 AI Whisperers Action Plan

_From 60 repos and $0 revenue to a focused, profitable operation_

**Created:** 2026-02-06  
**Owner:** Ivan + Nyx 🌙  
**Review:** Weekly

---

## Phase 0: EMERGENCY (Today - 2 hours)

### 🚨 P0-001: Rotate All Compromised API Keys

**File:** `/home/ai-whisperers/LangAi/scripts/utils/update_env.py`

| # | Service | Action | URL | Time |
|---|---------|--------|-----|------|
| 1 | **Anthropic** | Rotate key | https://console.anthropic.com/settings/keys | 2 min |
| 2 | **OpenAI** | Rotate key | https://platform.openai.com/api-keys | 2 min |
| 3 | **GitHub PAT** | Revoke + recreate | https://github.com/settings/tokens | 3 min |
| 4 | **Google** | Rotate key | https://console.cloud.google.com/apis/credentials | 2 min |
| 5 | Groq | Rotate key | https://console.groq.com/keys | 2 min |
| 6 | Tavily | Rotate key | https://tavily.com/dashboard | 2 min |
| 7 | Serper | Rotate key | https://serper.dev/dashboard | 2 min |
| 8 | Brave | Rotate key | https://brave.com/search/api/ | 2 min |
| 9 | Alpha Vantage | Rotate key | https://www.alphavantage.co/support/#api-key | 2 min |
| 10 | FMP | Rotate key | https://financialmodelingprep.com/developer/docs/ | 2 min |
| 11 | NewsAPI | Rotate key | https://newsapi.org/account | 2 min |
| 12 | Langfuse | Rotate both keys | https://cloud.langfuse.com | 2 min |
| 13 | LangChain | Rotate key | https://smith.langchain.com/settings | 2 min |

**After rotation:**
```bash
cd /home/ai-whisperers/LangAi
rm scripts/utils/update_env.py
git add -A
git commit -m "security: remove file with exposed credentials"
git push
```

**Then scrub git history:**
```bash
# Install BFG if needed
# java -jar bfg.jar --delete-files update_env.py
# Or use git filter-repo
pip install git-filter-repo
git filter-repo --path scripts/utils/update_env.py --invert-paths
git push --force
```

---

## Phase 1: CLEANUP (This Week - 4 hours)

### P1-001: Delete Empty/Useless Repos

**Repos to DELETE (via GitHub UI or gh CLI):**

```bash
# These are empty or useless
gh repo delete Ai-Whisperers/geoprot --yes
gh repo delete Ai-Whisperers/organization-template --yes
gh repo delete Ai-Whisperers/blueprint-code-once-deploy-everywhere --yes
gh repo delete Ai-Whisperers/scrapped-comments --yes
gh repo delete Ai-Whisperers/Information-Archive --yes
```

| Repo | Reason | Action |
|------|--------|--------|
| geoprot | No code | Delete |
| organization-template | Empty | Delete |
| blueprint-code-once-deploy-everywhere | Empty | Delete |
| scrapped-comments | Data, not code | Delete |
| Information-Archive | No purpose | Delete |

---

### P1-002: Archive Marketing Graveyard

**Repos to ARCHIVE (read-only, hidden from main view):**

```bash
# Archive via GitHub API
for repo in \
  outreach-automation \
  social-media-intelligence-marketing \
  feedbackScope-backend \
  Comment-Exctractor \
  Company-resarcher \
  linkedin-content-system \
  AI-powered-marketing-campaign-generator \
  cluster-template \
  clustering-for-ai-whisperers-hosting-and-deploys
do
  gh repo archive "Ai-Whisperers/$repo" --yes
done
```

| Repo | Last Activity | Action |
|------|---------------|--------|
| outreach-automation | Nov 2025 | Archive |
| social-media-intelligence-marketing | Nov 2025 | Archive |
| feedbackScope-backend | Nov 2025 | Archive |
| Comment-Exctractor | Nov 2025 | Archive |
| Company-resarcher | Dec 2025 | Archive |
| linkedin-content-system | Nov 2025 | Archive |
| AI-powered-marketing-campaign-generator | Dec 2025 | Archive |
| cluster-template | Unused | Archive |
| clustering-for-ai-whisperers-* | Nov 2025 | Archive |

---

### P1-003: Rename Misspelled Repos

```bash
gh repo rename Ai-Whisperers/Comment-Exctractor comment-extractor
gh repo rename Ai-Whisperers/Company-resarcher company-researcher
```

---

### P1-004: Local Cleanup

```bash
# Remove archived repos from local disk
cd /home/ai-whisperers
rm -rf outreach-automation social-media-intelligence-marketing \
       feedbackScope-backend Comment-Exctractor Company-resarcher \
       linkedin-content-system cluster-template

# Clean up Desktop (3.3GB!)
ls -la Desktop/
# Review and delete what's not needed

# What is moltbot? (2.0GB)
ls -la moltbot/
# If obsolete, remove it
```

---

## Phase 2: CONSOLIDATION (Week 2 - 6 hours)

### P2-001: Consolidate Research Repos (10 → 3)

**Target structure:**
```
ternary-vaes-bioinformatics/     # Flagship (keep)
├── src/
│   ├── core/                    # From ternary-engine
│   ├── encoders/                # From codon-encoder-*
│   └── toolkit/                 # From tnas-ternary-toolkit
├── analysis/                    # From ternary-vaes-analysis
└── docs/

3-adic-ml/                       # Foundation library (keep)

ultrametric-antigen-AI/          # Application (keep)
```

**Steps:**
1. Verify nothing unique in: ternary-engine, tnas-ternary-toolkit, codon-encoder-api, codon-encoder-VIH-focused
2. Copy unique code into flagship
3. Update imports
4. Archive old repos

```bash
# Example merge
cd /home/ai-whisperers/ternary-vaes-bioinformatics
mkdir -p src/encoders
cp -r ../codon-encoder-api/src/* src/encoders/
cp -r ../codon-encoder-VIH-focused/src/* src/encoders/hiv/
git add -A && git commit -m "feat: consolidate encoder repos"
```

**Archive after verification:**
```bash
for repo in \
  ternary-vaes-analysis \
  ternary-engine \
  tnas-ternary-toolkit \
  codon-encoder-api \
  codon-encoder-VIH-focused \
  predictive-additive-capacity-control-library \
  geoprot
do
  gh repo archive "Ai-Whisperers/$repo" --yes
done
```

---

### P2-002: Simplify Coordination Hierarchy

**Current (8 levels):**
```
COMPANY → PILLAR → PROJECT → REPO → EPIC → STORY → TASK → SUBTASK
```

**New (4 levels):**
```
PILLAR → PROJECT → EPIC → TASK
```

**Changes:**
- Remove COMPANY (implicit)
- Remove REPO (tracked in project metadata)
- Merge STORY into EPIC (stories become sections)
- Remove SUBTASK (just checklist items in task)

**New file structure:**
```
work-coordination/
├── README.md
├── TRACKER.md           # Auto-generated
│
├── healthcare/          # Pillar (was pillars/healthcare-saas/)
│   └── vete/           # Project
│       ├── PROJECT.md  # Overview + backlog
│       ├── v003.md     # Epic (was folder with 5 files)
│       └── v004.md     # Epic
│
├── research/
│   └── padic/
│       └── ...
│
└── agents/
```

**Epic file format (simplified):**
```markdown
# v003: Security & DevOps

**Status:** ⏳ 11/12  
**Target:** 2026-02-10

## CI/CD Pipeline ✅
- [x] T001: GitHub Actions workflow — Nyx
- [x] T002: Node.js matrix — Nyx
- [x] T003: Branch protection — Nyx

## Rate Limiting ✅
- [x] T001: Research options — Nyx
- [x] T002: Implement @upstash/ratelimit — Nyx

## Input Sanitization (1/2)
- [x] T001: Audit API routes — Nyx
- [ ] T002: Add Zod schemas (~180 routes) — Nyx ⏳

## Auth Hardening ✅
- [x] T001: Review Supabase config — Nyx
- [x] T002: Failed login monitoring — Nyx
```

---

### P2-003: Auto-Generate TRACKER.md

Create a script that generates TRACKER.md from epic files:

```bash
#!/bin/bash
# scripts/generate-tracker.sh

echo "# 📊 Work Tracker" > TRACKER.md
echo "" >> TRACKER.md
echo "_Auto-generated: $(date)_" >> TRACKER.md
echo "" >> TRACKER.md

for pillar in healthcare research; do
  echo "## ${pillar^}" >> TRACKER.md
  for project in $pillar/*/; do
    echo "### $(basename $project)" >> TRACKER.md
    for epic in $project/*.md; do
      # Parse epic and count tasks
      total=$(grep -c "^\- \[" "$epic" 2>/dev/null || echo 0)
      done=$(grep -c "^\- \[x\]" "$epic" 2>/dev/null || echo 0)
      echo "- $(basename $epic .md): $done/$total" >> TRACKER.md
    done
  done
done
```

Add to git pre-commit hook or cron.

---

## Phase 3: PRODUCT FOCUS (Week 2-3)

### P3-001: Vete Go-To-Market

**Goal:** 1 paying clinic by end of February

| Task | Owner | Deadline | Status |
|------|-------|----------|--------|
| Identify 10 vet clinics in Asunción | Ivan | Feb 8 | ⬜ |
| Create 1-page sales deck (Spanish) | Nyx | Feb 8 | ⬜ |
| Cold outreach to 10 clinics | Ivan | Feb 10 | ⬜ |
| Demo with 3 interested clinics | Ivan | Feb 14 | ⬜ |
| Pilot agreement with 1 clinic | Ivan | Feb 20 | ⬜ |
| Onboard pilot clinic | Ivan+Nyx | Feb 25 | ⬜ |

**Sales deck outline:**
1. The problem: Paper records, WhatsApp chaos, no insights
2. The solution: Vete — all-in-one clinic management
3. Features: Appointments, medical records, inventory, billing
4. Pricing: $50/month per clinic (intro rate)
5. CTA: Free 30-day pilot

---

### P3-002: Vete Production Hardening

**Before onboarding a real clinic:**

| Task | Effort | Priority |
|------|--------|----------|
| Complete Zod validation (T002) | 4h | HIGH |
| Add error monitoring (Sentry) | 2h | HIGH |
| Backup strategy for Supabase | 1h | HIGH |
| User documentation (Spanish) | 4h | MEDIUM |
| Mobile-responsive fixes | 2h | MEDIUM |
| Performance audit | 2h | LOW |

---

### P3-003: Kill Non-Essential Projects

**Pause/Archive:**
- Education pillar (courses-website, Courses-Content) → Archive
- Healthcare templates (psicologia-ia, Odontology) → Archive until Vete profitable
- Marketing repos → Already archived in P1

**Keep Active:**
- Vete (PRIMARY)
- work-coordination (meta)
- 3 research repos (maintenance only)

---

## Phase 4: SUSTAINABILITY (Month 2+)

### P4-001: Revenue Targets

| Month | Target | Clinics |
|-------|--------|---------|
| Feb 2026 | $50 | 1 pilot |
| Mar 2026 | $150 | 3 clinics |
| Apr 2026 | $500 | 10 clinics |
| Jun 2026 | $2,000 | 40 clinics |
| Dec 2026 | $5,000 | 100 clinics |

---

### P4-002: Agent Swarm Optimization

**Current cost:** ~$5-15/day (Opus + Sonnet sub-agents)

**Optimize:**
- Use Sonnet for all routine tasks (10x cheaper)
- Reserve Opus for complex decisions only
- Reduce heartbeat frequency (5min → 15min for workers)
- Kill unused cron jobs

```bash
# Disable expensive jobs
openclaw cron update --jobId erebus-worker --enabled false
openclaw cron update --jobId task-discovery --enabled false
```

---

### P4-003: Repo Target State

**From 60 → 15 repos:**

| Category | Repos | Names |
|----------|-------|-------|
| Products | 1 | Vete |
| Coordination | 1 | work-coordination |
| Research | 3 | ternary-vaes-bioinformatics, 3-adic-ml, ultrametric-antigen-AI |
| Tools | 3 | photos-to-kml, work-hours-automated-reports, local-models-server |
| Client | 2 | Taller_Ocampos, folyo |
| Private | 3 | legal, sarah-psychology, nico-duarte |
| Org | 2 | .github, LangAi (fixed) |
| **Total** | **15** | |

---

## Execution Timeline

```
Week 1 (Feb 6-9)
├── Day 1: EMERGENCY - Rotate all keys ⚡
├── Day 2: Delete 5 empty repos
├── Day 3: Archive 10 marketing repos
└── Day 4: Local cleanup

Week 2 (Feb 10-16)
├── Consolidate research repos
├── Simplify coordination hierarchy
├── Complete Vete v003 (Zod schemas)
└── Create sales deck

Week 3 (Feb 17-23)
├── Cold outreach to 10 clinics
├── Demo with interested clinics
└── Start v004 code quality

Week 4 (Feb 24-28)
├── Sign pilot agreement
├── Onboard first clinic
└── Celebrate first revenue 🎉
```

---

## Success Metrics

| Metric | Now | Week 2 | Month 1 | Month 3 |
|--------|-----|--------|---------|---------|
| Active repos | 60 | 30 | 15 | 15 |
| Exposed keys | 15 | 0 | 0 | 0 |
| Vete MRR | $0 | $0 | $50 | $500 |
| Test coverage | 85% | 90% | 90% | 95% |
| Agent cost/day | $10 | $8 | $5 | $5 |

---

## Daily Standup Template

```markdown
## Standup [DATE]

### Yesterday
- 

### Today
- 

### Blockers
- 

### Revenue Pipeline
- Leads: X
- Demos scheduled: X
- Pilots active: X
```

---

## Ownership

| Phase | Owner | Support |
|-------|-------|---------|
| P0: Emergency | Ivan | Nyx |
| P1: Cleanup | Nyx | Ivan approval |
| P2: Consolidation | Nyx | - |
| P3: Product | Ivan | Nyx |
| P4: Sustainability | Both | - |

---

_"The best time to delete 45 repos was 6 months ago. The second best time is today."_

— Nyx 🌙
