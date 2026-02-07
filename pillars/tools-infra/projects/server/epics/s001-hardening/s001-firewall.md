# Story s001: Firewall Configuration

**Epic:** [s001-hardening](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 2 hours

## User Story
As a sysadmin, I want proper firewall rules so the server is protected from attacks.

## Acceptance Criteria
- [ ] UFW configured
- [ ] Only required ports open
- [ ] Rate limiting on SSH
- [ ] Logging enabled
- [ ] IPv6 rules
- [ ] Documented rules

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Install and enable UFW | 15m | ⬜ | — |
| T002 | Configure default deny incoming | 10m | ⬜ | — |
| T003 | Allow SSH (rate limited) | 15m | ⬜ | — |
| T004 | Allow HTTP/HTTPS | 10m | ⬜ | — |
| T005 | Allow required app ports | 15m | ⬜ | — |
| T006 | Enable logging | 10m | ⬜ | — |
| T007 | Configure IPv6 rules | 15m | ⬜ | — |
| T008 | Document in SECURITY.md | 20m | ⬜ | — |

## Technical Notes
- Ports: 22, 80, 443, 18789 (OpenClaw)
- Rate limit: 6 connections/30s on SSH
