# Awesome AI Agent Workspaces

Tracking AI coworking / workspace products for **one-person companies** and **teams** — where AI agents are persistent teammates in a shared workspace, not one-off tools.

Each entry notes **who it's for**, **how you pay for the agents** (bring your own Claude/Codex subscription, or use the vendor's hosted cloud), the **agents it works with**, and **what makes it different**.

---

### [Paperclip](https://paperclip.ing)
**For:** Solo founders and teams running an autonomous "company of agents" across all functions — dev, marketing, ops — not just code.
**Agents:** Claude Code, Codex, Gemini, Cursor, and more (model-agnostic — anything that can take a heartbeat).
**Subscription:** Bring your own — open-source, self-hosted, no Paperclip account needed; you wire up your own agent runtimes.
**Different:** Runs agents like a real **company** — org chart with reporting lines, per-agent budgets with hard spend caps, and approval gates. "Business goals, not pull requests." · Free · MIT

### [Multica](https://multica.ai)
**For:** Engineering teams managing a mixed human + coding-agent workforce.
**Agents:** Claude Code, Codex, Copilot CLI, Gemini, Cursor, Kimi, and more (a local daemon auto-detects the CLIs you already have installed).
**Subscription:** Bring your own — agents run on your machine with your subscriptions. A hosted "Multica Cloud" exists but only for coordination, not agent compute.
**Different:** An **issue tracker** where agents are first-class assignees — they sit in the same dropdown as humans, open issues, comment, and run a full claim→complete lifecycle. Plus reusable Skills shared team-wide. · Free · Apache-2.0 (modified)

### [Slock](https://slock.ai)
**For:** Solo agent-native builders and lean teams who want to talk to agents like teammates.
**Agents:** Claude Code, Codex.
**Subscription:** Bring your own — agents run on your own hardware via a local daemon (`npx @slock-ai/daemon`), using your subscriptions. Free Hobby tier; paid Team/Business "coming soon."
**Different:** **Chat *is* the workspace** — Slack-style servers, channels, and DMs are the whole surface, and agents are persistent processes with their own memory. · Freemium

### [Hivespace](https://hivespace.app)
**For:** Teams doing general knowledge work — invite teammates and agents into a shared space (a solo user can spin one up, but it's built for collaboration).
**Agents:** Claude Code, Codex.
**Subscription:** Vendor cloud — a hosted web app; each workspace is a cloud-provisioned computer. (Login-gated; pricing not public.)
**Different:** Each workspace is a **self-contained cloud computer** with a shared file system — every agent gets a private sandbox, the team shares editable files, and agents build live web-app artifacts inside the workspace. · Closed

### [Vibe Kanban](https://github.com/BloopAI/vibe-kanban) *(sunsetting)*
**For:** Solo engineers or teams running multiple coding agents in parallel.
**Agents:** Claude Code, Codex, Gemini, Copilot, Amp, Cursor, and more.
**Subscription:** Both — run locally with your own agents/keys (free), *or* a hosted Cloud tier that provisioned agent compute (the ~$30/user/mo Pro plan, now winding down).
**Different:** A **kanban board** where each card spins up an isolated workspace (own git branch + terminal + dev server) — plan, run agents in parallel, review diffs inline, and open PRs. *(Sunsetting as of Apr 2026 → community-maintained, reverting to fully local.)* · Free · Apache-2.0

### [First-Tree](https://first-tree.ai)
**For:** Engineering teams (1–100 agents) who want their GitHub flow to stay put while agents share team knowledge (solo doesn't need it — the value is coordinating multiple people + agents).
**Agents:** Claude Code, Codex.
**Subscription:** Bring your own — open-source; the runtime runs agents on your machine with your subscriptions and routes messages through First-Tree. (`cloud.first-tree.ai` is the routing/coordination layer, or self-host it.)
**Different:** A git-native shared **context layer**, not an orchestrator — lives in your repo as the team's "living memory" (decisions, design, ownership) so agents stop cold-starting, and auto-routes GitHub issues/PRs to the right agent. · Free · Apache-2.0

---

*Verified against primary sources (live sites, GitHub, npm), June 2026. This space moves fast — verify before relying on pricing. Hivespace is login-gated, so its details are partially confirmed.*
