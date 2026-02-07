# Story s002: Mobile Authentication

**Epic:** [v008-mobile-app](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 4 hours

## User Story
As a user, I want to log in to the mobile app securely so I can access my data.

## Acceptance Criteria
- [ ] Login screen with email/password
- [ ] Secure token storage
- [ ] Biometric authentication option
- [ ] Auto-logout on token expiry
- [ ] Password reset flow

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Create LoginScreen UI | 45m | ⬜ | — |
| T002 | Implement auth API integration | 45m | ⬜ | — |
| T003 | Set up expo-secure-store for tokens | 30m | ⬜ | — |
| T004 | Add biometric auth with expo-local-authentication | 45m | ⬜ | — |
| T005 | Implement token refresh logic | 45m | ⬜ | — |
| T006 | Create ForgotPasswordScreen | 30m | ⬜ | — |

## Technical Notes
- Use same Supabase auth as web
- Biometric: Face ID / Touch ID / Fingerprint
