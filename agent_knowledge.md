# SuperClaw 2026: Agent Knowledge Base

*Extracted from the 2026 Super AI Agent Architecture Blueprint.*

## Core Philosophy

*   **One persistent body**: OpenClaw (Tool 3) running in Docker on a VPS or homelab server.
*   **MCP as nervous system**: Every capability is discovered and invoked dynamically—no hard-coded APIs.
*   **Hierarchical multi-agent system (MAS)**: One supervisor delegates to specialized sub-agents.
*   **Hybrid memory**: Short-term vector speed + lifelong structured knowledge + project-grounded silos.
*   **Model router**: The agent intelligently routes every sub-task to the optimal foundation model.
*   **Closed-loop self-improvement**: Every completed workflow is reflected upon, debugged, and versioned.

## Layered Architecture (MCP-Centric)

The architecture is built upon OpenClaw as the supervisor agent.

*   **Model Router MCP**: Routes to Claude Code (Coding/Execution), Gemini (Multimodal), Grok (Real-time X Sentiment), or ChatGPT o1 (General).
*   **Memory Core**: Pinecone/Milvus (Fast RAG), Obsidian Vault + Smart Connections (Lifelong Knowledge), NotebookLM (Project Silos).
*   **Tooling Hub MCP**: Composio (+500 SaaS), Supabase, GitHub, Puppeteer, DreamFactory, Tusk Drift.
*   **Analytics & Decision Engine**: Tellius (Root Cause), Databricks Genie + Julius.ai.
*   **Output & GEO Layer**: Frase / SEOBot (Content), GitHub + Vercel MCP (Deploy).
*   **Sequential Thinking MCP**: Planner and reflection mechanism.

## SuperClaw vs. OpenClaw

**Rule of thumb**: OpenClaw = the body and the hands. SuperClaw = the entire conscious organism.

| Aspect                  | OpenClaw (Raw Tool)                          | SuperClaw (Full Architecture)                              |
|-------------------------|----------------------------------------------|------------------------------------------------------------|
| What it is              | Single open-source agent                     | Full hierarchical multi-agent system built on OpenClaw     |
| Core Role               | Always-on “digital employee”                 | Supervisor body; orchestrates everything else              |
| Scope                   | Single agent (shell, browser, messaging)     | Entire 20-tool stack working as one living organism        |
| Intelligence            | Uses specified LLM                           | Intelligent Model Router MCP                               |
| Memory                  | Basic history                                | Pinecone + Obsidian + NotebookLM lifelong vault            |
| Reasoning               | Follows instructions in a loop               | Sequential Thinking MCP + self-critique loop               |
| Tool Access             | Built-in tools + basic MCP                   | Full MCP Tooling Hub (Composio + 500 SaaS, etc.)           |
| Autonomy Level          | Autonomous but single-threaded               | True multi-agent orchestration                             |
| Self-Improvement        | None native                                  | Root-cause analysis, fixes code, updates skills, deploys   |
| Use Case                | Personal assistant                           | Autonomous co-founder / entire digital workforce           |
| Deployment              | One Docker container                         | Same Docker + extra MCP servers + Obsidian vault           |

## Why SuperClaw Is "Super"

1.  Zero context switching.
2.  True agency (not just chat).
3.  Continuous self-improvement.
4.  Full ownership (local-first Obsidian + self-hosted MCP).
5.  Scales from solo power user to entire company digital workforce.
