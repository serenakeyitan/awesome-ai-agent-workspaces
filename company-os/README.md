# Company OS — Bot Organization

Portable org chart and spawn playbook for a multi-agent **company operating system**.

Any agent that can read this repo should be able to recreate the same organization: one orchestrator plus narrowly scoped specialists and a team channel.

## Quick Start (for agents)

1. Read [`ORG_CHART.md`](./ORG_CHART.md) for roles and reporting lines.
2. Follow [`SPAWN.md`](./SPAWN.md) to create missing agents, set profiles, and open the team channel.
3. Optionally install the repo skill at [`.cursor/skills/spawn-company-os/SKILL.md`](./.cursor/skills/spawn-company-os/SKILL.md).

## Design Principles

- **Scope like a job description** — one bot, one lane; clear in-scope / out-of-scope.
- **Trust after tools + context** — hand access, then let specialists run.
- **Invest and copy** — improve with feedback; reuse templates rather than bloating one chat.
- **Secrets stay in vault** — never paste API keys into chat history.

## Files

| File | Purpose |
| ---- | ------- |
| [`ORG_CHART.md`](./ORG_CHART.md) | Visual org chart (Mermaid) and role definitions |
| [`SPAWN.md`](./SPAWN.md) | Step-by-step spawn instructions for agents |
| [`org.manifest.json`](./org.manifest.json) | Machine-readable org structure |
| [`AGENTS.md`](./AGENTS.md) | Quick-start pointer for agents |
