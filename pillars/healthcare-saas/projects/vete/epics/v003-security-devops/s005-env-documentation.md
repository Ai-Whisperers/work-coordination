# S005: Environment Documentation

**Epic:** [v003-security-devops](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~2 hours total

---

## User Story

**As a** developer  
**I want** clear documentation of all environment variables  
**So that** I can set up the project without guessing

---

## Acceptance Criteria

- [ ] .env.example file created with all variables
- [ ] Each variable has a comment explaining its purpose
- [ ] README updated with setup instructions
- [ ] Sensitive values use placeholder format

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Create .env.example from current .env | 30m | ✅ | Nyx 🌙 |
| T002 | Add comments explaining each variable | 30m | ⬜ | — |
| T003 | Update README with env setup section | 30m | ⬜ | — |

---

## Task Details

### T001: Create .env.example

```bash
cd /home/ai-whisperers/Vete/web
# Extract variable names from .env (without values)
cat .env | sed 's/=.*/=/' > .env.example
```

Format:
```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
```

### T002: Add comments

```
# Supabase Configuration
# Get these from: https://supabase.com/dashboard/project/YOUR_PROJECT/settings/api
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key

# Service role key (KEEP SECRET - server only)
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
```

### T003: Update README

Add section:
```markdown
## Environment Setup

1. Copy `.env.example` to `.env`:
   \`\`\`bash
   cp .env.example .env
   \`\`\`

2. Fill in your Supabase credentials from the dashboard

3. Run the development server:
   \`\`\`bash
   npm run dev
   \`\`\`
```
