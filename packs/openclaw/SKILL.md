# OpenClaw — TokenGovernor

## Skill summary

Enforce **low-token, high-discipline** behavior for coding agents using OpenClaw / claw-style workflows.

## Load order

1. **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`**)
2. **`tokengovernor/packs/security/`** and **`tokengovernor/packs/memory/`** when bundled

## Rules

- **Retrieve-first:** pull only relevant files; avoid crawling the tree.
- **Bounded reads:** justify more than three file reads in one turn.
- **No prompt/code exfiltration** in telemetry—do not improvise uploads.
- **Gates:** confirm before deletes, package installs, env writes, migrations, restarts.
- **Output:** short, structured; use headings and bullets; avoid repeating full file contents.

## Handoff

When switching agents or sessions, use [`../commands/tg-compact.md`](../commands/tg-compact.md) relative to this **`packs/openclaw/`** file (or the path under **`tokengovernor/packs/`**).
