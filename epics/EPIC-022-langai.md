# EPIC-022: LangAi — Language Processing Toolkit

**Owner:** Available  
**Status:** URGENT (Security Issue)  
**Priority:** HIGH  
**Created:** 2026-02-06  
**Repo:** https://github.com/Ai-Whisperers/LangAi  
**Local:** `/home/ai-whisperers/LangAi`

---

## Overview

AI language processing toolkit with LangChain integration.

## 🚨 SECURITY ALERT

**Credential exposure detected!**
- Groq API key exposed in `update_env.py:19`
- Langfuse credentials exposed in `update_env.py:33`

**IMMEDIATE ACTION REQUIRED:**
1. Rotate Groq API key
2. Rotate Langfuse credentials
3. Remove secrets from code
4. Add proper .env handling

## Tasks

### Security (SEC) — CRITICAL

| ID | Task | Effort | Status |
|----|------|--------|--------|
| LNG-SEC-001 | Remove exposed Groq key from code | LOW | ⬜ |
| LNG-SEC-002 | Remove exposed Langfuse creds | LOW | ⬜ |
| LNG-SEC-003 | Add .env.example with placeholders | LOW | ⬜ |
| LNG-SEC-004 | Add .env to .gitignore | LOW | ⬜ |
| LNG-SEC-005 | Document secret rotation in README | LOW | ⬜ |

### Documentation (DOC)

| ID | Task | Effort | Status |
|----|------|--------|--------|
| LNG-DOC-001 | Update README with setup | LOW | ⬜ |
| LNG-DOC-002 | Document LangChain integration | MEDIUM | ⬜ |

### Infrastructure (INFRA)

| ID | Task | Effort | Status |
|----|------|--------|--------|
| LNG-INFRA-001 | Add CI with secret scanning | MEDIUM | ⬜ |
| LNG-INFRA-002 | Update dependencies | LOW | ⬜ |

---

## Priority Order

1. **LNG-SEC-001** through **LNG-SEC-005** — Fix security issues FIRST
2. Then documentation
3. Then infrastructure

## Definition of Done

- [ ] No secrets in code
- [ ] .env.example exists
- [ ] .gitignore includes .env
- [ ] CI includes secret scanning
- [ ] Keys rotated and documented
