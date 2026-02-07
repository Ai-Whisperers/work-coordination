# REPO_GOALS.md — Human-Defined Direction

_This is the ONE place where humans define what each repo should achieve._
_AI agents autonomously handle everything else: planning, coding, testing, docs._

**Last updated:** 2026-02-07
**Updated by:** Ivan

---

## How This Works

1. **Humans** define the goal and priority for each repo below
2. **AI** reads this file and autonomously:
   - Plans work to achieve the goal
   - Identifies technical improvements
   - Creates tickets, executes work
   - Reports progress

**AI can autonomously do:**
- Fix bugs, tests, lint, types
- Improve code quality
- Add documentation
- Refactor for clarity
- Update dependencies
- Security fixes
- Performance improvements
- Anything that adds value toward the goal

**AI will ask humans for:**
- Changing the goal/direction
- Major architectural decisions
- Removing features
- External communications (emails, messages to customers)

---

## Active Repos

### 🔴 P0 — Critical (Daily attention)

#### Vete
- **Goal:** Get first paying clinic by end of February 2026
- **Direction:** Focus on sales, demo-readiness, onboarding flow
- **AI Focus:** 
  - Code quality (0 lint errors, full type safety)
  - Test coverage (all routes tested)
  - Security hardening
  - Sales materials generation
- **Constraints:** No breaking changes to production

---

### 🟡 P1 — High (Weekly attention)

#### work-coordination
- **Goal:** Keep all work organized and tracked
- **Direction:** Self-maintaining, auto-updating
- **AI Focus:**
  - Auto-generate tickets from discoveries
  - Keep TRACKER.md current
  - Archive completed work
- **Constraints:** None

#### ternary-vaes-bioinformatics
- **Goal:** Publish research paper, clean up for open-source release
- **Direction:** Documentation, validation, reproducibility
- **AI Focus:**
  - Improve documentation
  - Add examples
  - Fix any failing tests
  - Clean up code
- **Constraints:** Don't change core algorithms without discussion

---

### 🟢 P2 — Medium (Monthly attention)

#### psicologia-ia
- **Goal:** Template for psychology practices with AI tools
- **Direction:** Clean, reusable, well-documented
- **AI Focus:**
  - Template cleanup
  - Documentation
  - Remove hardcoded values
- **Constraints:** Keep it generic/reusable

#### photos-to-kml
- **Goal:** Working tool for John's Google Photos → KML use case
- **Direction:** John is primary user, follow his requests
- **AI Focus:**
  - Code quality
  - Documentation
- **Constraints:** Check with John before major changes

---

### 🔵 P3 — Low (Quarterly attention)

#### courses-website
- **Goal:** FPUNA course platform
- **Direction:** Maintenance mode
- **AI Focus:** Bug fixes, dependency updates only
- **Constraints:** Minimal changes

#### ultrametric-antigen-AI, 3-adic-ml, ternary-vaes-analysis, ternary-engine
- **Goal:** Research support repos for main ternary-vaes
- **Direction:** Keep working, support main repo
- **AI Focus:** Dependency updates, test fixes
- **Constraints:** Minimal active development

---

### ⚫ P4 — Archive (No active work)

#### Odontology, mike (physio), marketing-strategy, ai-whisperers-portfolio
- **Goal:** None currently
- **Direction:** Archived/dormant
- **AI Focus:** None (skip in discovery)
- **Constraints:** Do not work on these

---

## Adding a New Repo

To add a repo for AI to work on:

```markdown
#### repo-name
- **Goal:** What should this repo achieve?
- **Direction:** High-level strategy
- **AI Focus:** What AI should improve
- **Constraints:** What AI should NOT do
```

---

## Changing Direction

To change a repo's direction:
1. Edit this file
2. Commit with message: `goals: update <repo-name> direction`
3. AI will pick up changes on next discovery run

---

_AI agents read this file at startup and during discovery._
_All technical work is autonomous. Strategic direction is human-controlled._
