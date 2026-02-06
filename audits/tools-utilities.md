# Tools & Utilities Assessment

_6 utility repositories — mixed health_

---

## Overview

| Repo | Status | Verdict |
|------|--------|---------|
| LangAi | 🚨 SECURITY | Fix NOW |
| photos-to-kml | 🟢 Active | Keep |
| work-hours-automated-reports | 🟢 Active | Keep |
| yt-transcript-headless | 🟡 Stale | Evaluate |
| local-models-server | 🟡 Stale | Evaluate |
| mcp-for-deploys | 🟡 Stale | Evaluate |

---

## LangAi 🚨

**STATUS: CRITICAL SECURITY ISSUE**

### The Problem

```python
# update_env.py:19 — EXPOSED
GROQ_API_KEY = "gsk_xxxxx..."

# update_env.py:33 — EXPOSED  
LANGFUSE_SECRET_KEY = "sk-lf-xxxxx..."
```

**These credentials are in version control. Anyone can see them.**

### Immediate Actions

1. **Rotate Groq key:** https://console.groq.com/keys
2. **Rotate Langfuse key:** https://cloud.langfuse.com
3. **Remove from code:** Replace with environment variables
4. **Add .env.example:** Document required vars
5. **Add to .gitignore:** Prevent future leaks

### Why This Matters

- Groq API key = someone can run LLM calls on your account
- Langfuse key = someone can access your LLM observability data
- Credential leaks = amateur hour. Fix it.

---

## photos-to-kml ⭐⭐⭐

**STATUS: Active, Healthy**

| Attribute | Value |
|-----------|-------|
| Owner | John (Ivan's father) |
| Language | Python |
| Last push | Feb 2026 |
| Purpose | Extract GPS from photos → KML for Google Earth |

### Assessment

- **Does what it says:** Simple, focused utility
- **Active development:** John is using Cursor Agent on it
- **Clear use case:** Photo geolocation visualization

### Verdict

Keep. It's a good example of a focused tool that solves one problem.

---

## work-hours-automated-reports ⭐⭐⭐

**STATUS: Active, Useful**

| Attribute | Value |
|-----------|-------|
| Language | Python |
| Last push | Today |
| Purpose | Clockify + Azure DevOps time reporting |

### Assessment

- **Practical:** Actually used for work hour tracking
- **Integration:** Connects two real tools
- **Recent activity:** Someone is using this

### Verdict

Keep. Internal tooling that provides real value.

---

## yt-transcript-headless ⭐⭐

**STATUS: Stale but Potentially Useful**

| Attribute | Value |
|-----------|-------|
| Language | TypeScript |
| Last push | Dec 2025 |
| Purpose | YouTube transcript extraction via Playwright |

### Assessment

- **Niche:** Specific use case (transcript extraction)
- **Tech:** Playwright for headless automation
- **RAG/MCP:** Mentions RAG and MCP support

### Questions

- Is this being used anywhere?
- Does it work with current YouTube?
- Is there a simpler alternative?

### Verdict

Evaluate. If actively used, keep. If not, archive.

---

## local-models-server ⭐⭐

**STATUS: Stale**

| Attribute | Value |
|-----------|-------|
| Language | PowerShell (primary) |
| Last push | Jan 2026 |
| Purpose | GGUF/ONNX model serving |

### Assessment

- **Good idea:** Local model serving is useful
- **Weird language:** Why is PowerShell the primary language?
- **Stale:** No activity in 3 weeks

### Questions

- Who uses this?
- Does it work on Linux?
- Is there a better alternative (Ollama, llama.cpp)?

### Verdict

Evaluate. Local models are relevant but Ollama might be better.

---

## mcp-for-deploys ⭐⭐

**STATUS: Unclear**

| Attribute | Value |
|-----------|-------|
| Language | TypeScript |
| Last push | Dec 2025 |
| Description | None |

### Assessment

- **MCP undefined:** What is MCP? Model Context Protocol?
- **No description:** Can't tell what this does
- **Stale:** 2 months since activity

### Verdict

Document or archive. If nobody knows what it does, it's not useful.

---

## Summary

| Action | Repos |
|--------|-------|
| 🚨 Fix immediately | LangAi |
| ✅ Keep | photos-to-kml, work-hours-automated-reports |
| ❓ Evaluate | yt-transcript-headless, local-models-server, mcp-for-deploys |

---

## Priority Task

**LangAi credential rotation is BLOCKING. Do it now.**

```bash
# Check current exposure
cd /home/ai-whisperers/LangAi
grep -n "gsk_\|sk-lf" . -r

# After rotation, update to use env vars
# .env.example should have:
# GROQ_API_KEY=your_key_here
# LANGFUSE_SECRET_KEY=your_key_here
```
