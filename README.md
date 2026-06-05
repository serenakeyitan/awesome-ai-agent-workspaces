# Awesome AI Agent Workspaces [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of **"Slack for AI agents"** — platforms where AI agents are persistent **teammates** in a shared workspace, not one-off tools.

This list covers the emerging category of **multiplayer human + agent workspaces** and **managed-agent control planes**: products where people and multiple AI agents collaborate in shared channels, boards, canvases, or org charts — with shared context, task coordination, and human-in-the-loop governance.

It is intentionally **tightly scoped**. This is *not* a list of general multi-agent frameworks (CrewAI, AutoGen, LangGraph) or single autonomous agents (Devin, AutoGPT). It's specifically about the *workspace* — the connective tissue where humans and agent teams work side by side.

## Contents

- [What counts](#what-counts)
- [Commercial workspaces](#commercial-workspaces)
- [Open-source & self-hosted](#open-source--self-hosted)
- [Coding-agent workspaces](#coding-agent-workspaces)
- [Shared context & memory](#shared-context--memory)
- [Comparison table](#comparison-table)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## What counts

To be on this list, a project should treat AI agents as **persistent participants in a shared workspace** alongside humans (and/or other agents). Concretely, at least one of:

- **Multiplayer chat** — agents live in channels / DMs / threads as teammates you `@mention`.
- **Shared board / canvas** — agents and humans pull from the same task queue, kanban, or spatial canvas.
- **Managed agent team** — you "hire," assign, budget, and supervise a roster of agents (an org chart or control plane).
- **Shared context layer** — a substrate that gives every agent the same persistent, owned context a human teammate would have.

Single-agent autopilots and library-only frameworks are out of scope (see [Related lists](#related-lists) for those).

Legend: 🟢 open source · 🟡 source-available · 🔴 closed · ⭐ GitHub stars · 🧪 experimental

---

## Commercial workspaces

Hosted platforms where humans and agents collaborate as co-contributors.

- **[Dust](https://dust.tt)** 🟢 — *"Multiplayer AI for human-agent collaboration."* A shared workspace where people and agents work as equal co-contributors over the same knowledge, tools, conversations, and notifications. Explicitly built against "single-player AI." The clearest commercial expression of this category. ([github.com/dust-tt/dust](https://github.com/dust-tt/dust), MIT, ⭐ 1.4k)
- **[Salesforce Agentforce in Slack](https://slack.com/ai-agents)** 🔴 — *"Turn agents into teammates."* Agents (Agentforce + third-party) become full members of Slack channels, DMs, and threads — `@mention` an agent like any teammate for context and autonomous action. The canonical "Slack for AI agents," shipped by Slack itself.
- **[Relevance AI](https://relevanceai.com)** 🔴 — *"The home of the AI Workforce."* Build and manage teams of specialized agents (e.g. an SDR "workforce" of researcher + copywriter + sender agents) running human-authored playbooks. Leans toward a managed agent control plane rather than a shared chat.
- **[Sema4.ai](https://sema4.ai/products/work-room/)** 🔴 — *"Work Room — where teams work with AI agents."* An enterprise, SSO-gated workspace where business users find, chat with, and supervise both conversational and autonomous "worker" agents, with visibility into how agents plan and reason.
- **[Asana AI Teammates](https://asana.com/product/ai)** 🔴 — Embeds ~30 prebuilt "AI Teammates" into Asana's work graph so teams and agents run workflows together with humans kept in the loop. The work-management take on human + agent teams.

## Open-source & self-hosted

Self-hostable platforms — most run agents on your own machines so code/compute stay local.

- **[Paperclip](https://paperclip.ing)** 🟢 — *"The open-source app everyone uses to manage agents at work."* Organize AI agents into a structured "company": org charts, roles, reporting lines, goals, per-agent budgets with hard spend caps, ticketing/audit trails, and human approval gates. Model-agnostic (Claude, OpenAI, Gemini, Cursor…). ([github.com/paperclipai/paperclip](https://github.com/paperclipai/paperclip), MIT, ⭐ 69k)
- **[Multica](https://multica.ai)** 🟢 — *"Project management for human + agent teams."* Assign issues to an agent like a colleague; it picks up work, writes code, and reports blockers on a board alongside humans. Adds reusable "skills" and **Squads** (a lead agent delegates to members). Execution stays on your machine — code never passes through Multica. Supports Claude Code, Codex, Copilot CLI, Gemini, Cursor and more. ([github.com/multica-ai/multica](https://github.com/multica-ai/multica), ⭐ 35k)
- **[Slock](https://slock.ai)** 🔴 — *"Where humans and AI agents build together."* A real-time platform with servers, channels, and DMs where agents are equal teammates with persistent memory and identity. Agents run on your own machines via a lightweight daemon (`npx @slock-ai/daemon`); supports Claude, Codex, Kimi. Self-hosted execution but **closed-source** (proprietary daemon). Free to start.
- **[Hivespace](https://hivespace.app)** 🔴 — A multi-agent workspace delivered as a login-gated web app (PWA); sign-in via GitHub or Google. Product details are behind authentication and not publicly documented. *(Listed for completeness — verify before relying on specifics.)*

## Coding-agent workspaces

The literal "Slack / Kanban / Figma for coding agents" — orchestrate multiple coding agents (Claude Code, Codex, Gemini) working in parallel on isolated git worktrees.

- **[Claude Code — Agent Teams](https://code.claude.com/docs/en/agent-teams)** 🔴 🧪 — Coordinate multiple Claude Code sessions as a team: a lead spawns teammates (each its own context window) that share a **task list** (claim/complete with file-locking) and a **mailbox** to message each other directly. Native to Claude Code; experimental and off by default (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`).
- **[Vibe Kanban](https://github.com/BloopAI/vibe-kanban)** 🟢 — *"Get 10X more out of Claude Code, Codex or any coding agent."* A Kanban board to plan and run coding agents in parallel — each task on its own branch with diff review, inline comments, a preview browser, and PR/merge flow. Now community-maintained under Apache 2.0 (Bloop wound down in April 2026; reverting to a fully local architecture). (Apache-2.0, ⭐ 27k)
- **[Agor](https://agor.live)** 🟡 — *"Team command center for all things agentic."* A multiplayer **spatial canvas** ("Figma for AI coding agents") where agents run side by side on isolated worktrees, with live cursors, a facepile, scoped comments, and shared sessions. Drag a session into a zone ("Needs Tests," "Ready for Review") to prompt it. The strongest *multiplayer* fit among dev tools. ([github.com/preset-io/agor](https://github.com/preset-io/agor), BSL 1.1 → Apache-2.0 in 2029, ⭐ 1.2k)
- **[Conductor](https://conductor.build)** 🔴 — *"Run a team of coding agents on your Mac."* A native Mac app that runs multiple Claude Code / Codex agents at once, each in an isolated git worktree on its own branch, with one pane to watch, review, and merge. Single-operator (no shared human-to-human canvas) but a clean local team-of-agents runner. Free; bring your own subscription.

## Shared context & memory

The layer *beneath* orchestration: give every agent the same persistent, owned context a human teammate would have.

- **[First-Tree](https://first-tree.ai)** 🟢 — *"Shared Context for AI Agent Teams."* A Git-native, tree-structured knowledge substrate that stores a team's decisions, conventions, ownership, and constraints as versioned, *owned* context living in your own GitHub. Rather than executing work, it routes tasks to the right agent, hands it the same context the team has, and loops humans in only when the rules say so. ([github.com/agent-team-foundation/first-tree](https://github.com/agent-team-foundation/first-tree), MIT)

## Comparison table

| Project | Shape | Open source | Agents run | Stars |
|---|---|---|---|---|
| [Dust](https://dust.tt) | Multiplayer chat workspace | 🟢 MIT | Hosted | ⭐ 1.4k |
| [Agentforce in Slack](https://slack.com/ai-agents) | Agents in Slack | 🔴 | Hosted | — |
| [Relevance AI](https://relevanceai.com) | AI workforce control plane | 🔴 | Hosted | — |
| [Sema4.ai](https://sema4.ai) | Enterprise work room | 🔴 | Hosted | — |
| [Asana AI Teammates](https://asana.com/product/ai) | Work-management board | 🔴 | Hosted | — |
| [Paperclip](https://paperclip.ing) | Agent org chart + governance | 🟢 MIT | Local / self-host | ⭐ 69k |
| [Multica](https://multica.ai) | PM board for human+agent teams | 🟢 | Local / self-host | ⭐ 35k |
| [Slock](https://slock.ai) | Servers / channels / DMs | 🔴 | Local daemon | — |
| [Hivespace](https://hivespace.app) | Multi-agent workspace (gated) | 🔴 | — | — |
| [Claude Code Agent Teams](https://code.claude.com/docs/en/agent-teams) | Coding-agent team | 🔴 🧪 | Local | — |
| [Vibe Kanban](https://github.com/BloopAI/vibe-kanban) | Kanban for coding agents | 🟢 Apache-2.0 | Local | ⭐ 27k |
| [Agor](https://agor.live) | Multiplayer canvas | 🟡 BSL 1.1 | Local | ⭐ 1.2k |
| [Conductor](https://conductor.build) | Mac app, worktree per agent | 🔴 | Local | — |
| [First-Tree](https://first-tree.ai) | Shared context substrate | 🟢 MIT | n/a (context layer) | — |

> Star counts and details are point-in-time (June 2026) and this is a fast-moving space — verify before citing.

## Related lists

For the broader landscape this list deliberately excludes:

- [awesome-agent-orchestrators](https://github.com/andyrewlee/awesome-agent-orchestrators) — multi-agent orchestration projects (broader, includes long-tail OSS).
- Multi-agent **frameworks** (out of scope here): [CrewAI](https://github.com/crewAIInc/crewAI), [AutoGen](https://github.com/microsoft/autogen), [MetaGPT](https://github.com/FoundationAgents/MetaGPT), [LangGraph](https://github.com/langchain-ai/langgraph), [OpenAI Agents SDK](https://github.com/openai/openai-agents-python), [CAMEL](https://github.com/camel-ai/camel).
- Interop **standards**: [MCP](https://modelcontextprotocol.io) (Anthropic), [A2A](https://github.com/google/A2A) (Google).

## Contributing

Contributions welcome! Please open a PR. To keep this list high-signal:

1. The project must fit [What counts](#what-counts) — a *workspace* for human + agent teams, not a framework or single agent.
2. One entry per line: **bold linked name**, open-source/license badge, then a factual one-to-two-sentence description.
3. **No marketing fluff.** Describe what the product actually does. Tag closed-source honestly.
4. Verify claims against a primary source (the live site, GitHub, or npm) before submitting.

---

*Inspired by the [awesome](https://github.com/sindresorhus/awesome) manifesto. To the extent possible under law, contributors have waived all copyright to this list.*
