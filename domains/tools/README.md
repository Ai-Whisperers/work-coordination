# 🛠️ Tools Domain

Standalone utilities and tool repositories.

---

## Active

### LangAi ⚠️

**AI language processing toolkit**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/LangAi](https://github.com/Ai-Whisperers/LangAi) |
| Local | `/home/ai-whisperers/LangAi` |
| Status | 🚨 **SECURITY ISSUE** |

**⚠️ URGENT:** Credentials exposed in code!
- Groq API key in `update_env.py:19`
- Langfuse creds in `update_env.py:33`

| ID | Task | Priority | Status |
|----|------|----------|--------|
| LNG-SEC-001 | Remove Groq API key | CRITICAL | ⬜ |
| LNG-SEC-002 | Remove Langfuse creds | CRITICAL | ⬜ |
| LNG-SEC-003 | Add .env.example | HIGH | ⬜ |

---

### photos-to-kml 📸

**GPS metadata → Google Earth KML**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/photos-to-kml](https://github.com/Ai-Whisperers/photos-to-kml) |
| Local | `/home/ai-whisperers/photos-to-kml` |
| Owner | Atlas 🗼 (John's project) |
| Status | Active development |

John (Ivan's father) is actively developing this with Cursor Agent.

---

## Maintenance

### yt-transcript-headless

**YouTube transcript extraction**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/yt-transcript-headless](https://github.com/Ai-Whisperers/yt-transcript-headless) |
| Status | Stable |

---

### local-models-server

**ONNX/GGUF model serving**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/local-models-server](https://github.com/Ai-Whisperers/local-models-server) |
| Status | Stable |

---

### mcp-for-deploys

**MCP deployment tools**

| Attribute | Value |
|-----------|-------|
| Repo | [Ai-Whisperers/mcp-for-deploys](https://github.com/Ai-Whisperers/mcp-for-deploys) |
| Status | Stable |

---

## Infrastructure Tools

These are in the `infrastructure/` section:
- .github (org templates)
- organization-template
- blueprint-code-once-deploy-everywhere
- deploy-automated-blueprint
- cluster-template
