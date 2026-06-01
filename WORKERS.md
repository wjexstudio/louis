# Worker Agents — Directory & Capacity

**Last updated:** 2026-06-01 11:28 น. (GMT+7)

---

## Active Roster

| Agent | Role | Capacity | Status | Access Method / Scope | Last Report |
|---|---|---|---|---|---|
| (system) | Manager (Claude) | — | active | Local (in-session) | managing |
| (TBD) | Developer | 0/5 | not deployed | TBD (Local / MCP / API) | — |
| (TBD) | Content Creator | 0/5 | not deployed | TBD (Local / MCP / API) | — |

---

## Capacity Model

Each agent has a max queue (e.g., 0/5 tasks):
- **0/5** = idle, ready for work
- **3/5** = busy, can take 2 more
- **5/5** = at capacity, new work queues

---

## Access Method / Scope

How to reach each agent (future-proof for different deployment modes):

- **Local** — Agent runs in this session (e.g., Claude Code)
- **MCP** — Agent accessible via Model Context Protocol (headless)
- **API** — Agent accessible via HTTP API (remote, scalable)

---

## How to add an agent

1. Add row to roster above (no separate folder needed for MVP)
2. Set Access Method based on deployment
3. Update Capacity when taking new work

---

## Current Agents

- **claude-code** (Manager) — local session

---

*Capacity tracking helps Claude (Manager) balance load and know who to delegate to.*
