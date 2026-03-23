# SuperClaw 2026: Agent Skills & Workflows

*Extracted from the 2026 Super AI Agent Architecture Blueprint.*

## Core Implementation Skills (Agentic Ecosystem)

### 1. Master Planner (Supervisor & Model Router)
*   Extend OpenClaw with a custom MCP server: `superclow-router`.
*   Maintain a capability matrix for routing logic (e.g., “code execution → Claude Code”).
*   Use Sequential Thinking MCP to decompose complex tasks before delegating to sub-agents.

### 2. Knowledge Agents (Memory Core Integration)
*   Index notes, workflows, and embeddings in Pinecone/Milvus for fast semantic retrieval.
*   Use Obsidian with Smart Connections + Copilot for Git-backed lifelong knowledge synthesis.
*   Auto-create NotebookLM projects for new initiatives; sync back to Obsidian via MCP bridge to ground all agent reasoning.

### 3. Skills Agents (Action & Tooling Hub)
*   Utilize Composio MCP + individual domain MCP servers (Supabase, GitHub, Puppeteer, etc.) as narrow executor "muscles."
*   Auto-generate missing REST endpoints using DreamFactory in sandboxed operations.
*   Auto-test endpoints using Tusk Drift.

### 4. Tandem Agents (Self-Improvement Loop)
Run peer-to-peer reflection loops after every workflow:
1.  Critique performance using Sequential Thinking MCP (Maker-Checker loop).
2.  Perform root-cause analysis on failures via Tellius.
3.  Generate improved prompts or new sub-agent skills via Claude Code.
4.  Commit changes via GitHub MCP and restart sub-agent.

### Security & Governance
*   Run all MCP servers read-only where possible.
*   Use OAuth 2.1 and isolated Docker networks.
*   Log every tool invocation with "Audit MCP" server.
*   Continuously validate new APIs with Tusk Drift.

---

## Signature Autonomous Workflows

### A. Data-to-Publish Pipeline
*(Original workflow from source document)*

### B. AI-Assisted Engineering Stack
*(Original workflow from source document)*

### C. Researcher’s Synthesis Loop
*(Original workflow from source document)*

### D. Autonomous Product Launch
Grok trend → Puppeteer scrape → Tellius gap analysis → Claude Code builds app → DreamFactory APIs → Tusk Drift tests → Frase content → SEOBot pSEO pages → Vercel deploy.

### E. Personal Life OS
Voice note → Gemini transcribe → Julius analysis → Obsidian link → NotebookLM Audio Overview → OpenClaw books calendar.

### F. Self-Evolving Research Agent
Vague goal → Puppeteer papers → NotebookLM ground → Julius stats → Obsidian archive → capability matrix update.

---

## Deployment & Setup Commands

### Deployment Checklist (One-Command SuperClaw)

```bash
# On your VPS
docker run -d \
 -v ~/superclaw-vault:/root/.obsidian \
 -e MCP_SERVERS="supabase,github,puppeteer,composio,pinecone" \
 openclaw/superclaw:latest
```

*Then point a Telegram/WhatsApp bot to the instance.*

### Migration: OpenClaw → SuperClaw in 15 Minutes
1.  Keep existing OpenClaw container.
2.  Add the `superclow-router` MCP server.
3.  Point Obsidian vault at `~/superclaw-vault`.
4.  Enable Smart Connections + Copilot plugins.
5.  Add the Master Supervisor prompt template.
6.  Restart to run SuperClaw.

### Obsidian Integration & Second-Brain Setup (Tool 19)
**Mandatory Plugins:**
*   Smart Connections (local vectors)
*   Copilot / AI Assistant
*   Dataview
*   Obsidian-Git or Remotely Sync (AES-256)

**Daily Routine:**
*   SuperClaw outputs land in `Inbox/`
*   Smart Connections auto-links
*   Weekly review query: `LIST WHERE contains(file.outlinks, "SuperClaw")`
