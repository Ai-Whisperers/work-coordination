# S004: Auth Hardening

**Epic:** [v003-security-devops](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~3 hours total

---

## User Story

**As a** user  
**I want** my account to be secure  
**So that** my data is protected from unauthorized access

---

## Acceptance Criteria

- [ ] Token expiry settings reviewed and documented
- [ ] Session invalidation works on password change
- [ ] Failed login attempts are logged
- [ ] No sensitive data in JWT payload
- [ ] Refresh token rotation enabled

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Review Supabase auth configuration | 1h | ⬜ | — |
| T002 | Implement failed login monitoring | 2h | ⬜ | — |

---

## Task Details

### T001: Review Supabase auth configuration

**Check in Supabase Dashboard → Authentication → Settings:**

- [ ] JWT expiry time (default 3600s = 1hr)
- [ ] Refresh token rotation enabled?
- [ ] Session timeout settings
- [ ] Password requirements
- [ ] Rate limiting on auth endpoints

**Document current settings in:**
`/home/ai-whisperers/Vete/web/docs/AUTH.md`

---

### T002: Implement failed login monitoring

**Options:**

1. **Supabase Auth Hooks** (recommended)
   - Use `onAuthStateChange` to detect failures
   - Log to Supabase table or external service

2. **Custom middleware**
   - Wrap auth endpoints
   - Track by IP/email

**Basic implementation:**

```typescript
// lib/auth/monitoring.ts
export async function logAuthAttempt(
  email: string,
  success: boolean,
  ip: string
) {
  await supabase.from("auth_logs").insert({
    email,
    success,
    ip,
    timestamp: new Date().toISOString(),
  });
}

// Alert on 5+ failures from same IP/email in 15 minutes
```

**Schema:**
```sql
create table auth_logs (
  id uuid primary key default gen_random_uuid(),
  email text,
  success boolean,
  ip text,
  timestamp timestamptz default now()
);
```

---

## Security Notes

- Don't reveal whether email exists in error messages
- Consider account lockout after N failures
- Log but don't expose IP addresses to users
