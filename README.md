# dsh-memory

Cross-session memory: remember/recall/forget keyed to a workspace token — a later session, or a different machine, picks up where you left off.

## What & why

Developer-preview harnesses forget everything between runs. `remember`/`recall`/`forget` persist against a free anonymous workspace token (issued automatically on first call), so state survives restarts, machines, and even switching harnesses — the same token works from Claude Code or any MCP client.

Every set ships `what_can_you_do` — describe a task in any language, get the exact tool + a ready-to-run call.

## Install

```sh
dsh plugin --profile <your-profile> add github:mario03690/dsh-memory
```

Thin config layer only (one `@deepseek-ai/dsh-mcp-client` row, shipped as `cordis.patch.yml`) — no tool code runs on your machine. Built against the MCP client config shape of the dsh v0.1 developer preview (2026-08-13); if a later preview changes it, open an issue for a same-day fix.

## Cost, quota, privacy

Free anonymous quota, no signup; every response reports its exact USD cost; failed calls are not charged. Documents are processed in memory and not retained. The config URL carries `?s=dsh-memory` — a channel tag identifying the install path, not you.

**Disclosure:** built and run by the team behind [ainetcafe.com](https://ainetcafe.com) — our own service, free tier plus paid usage. Full bundle (everything at once): [dsh-netcafe](https://github.com/mario03690/dsh-netcafe). MIT.
