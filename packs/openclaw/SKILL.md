# OpenClaw — TokenGovernor

## Summary

Enforce **low-token, high-discipline** behavior for coding agents on OpenClaw / claw-style workflows.

---

## Load order

1. **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`**)
2. **`tokengovernor/packs/security/`** and **`tokengovernor/packs/memory/`** when bundled with this skill

---

## Rules

- **Retrieve first** — open only relevant files; avoid crawling the tree without a hypothesis.
- **Bounded reads** — justify more than three file reads in a single turn.
- **No improvised telemetry uploads** — do not send prompts or code to unapproved endpoints.
- **Gates** — confirm before deletes, package installs, environment writes, migrations, or service restarts.
- **Output** — short, structured, headings and bullets; do not repeat full file bodies unless asked.

---

## Session handoff

When switching agents or sessions, use [`../commands/tg-compact.md`](../commands/tg-compact.md) relative to this **`packs/openclaw/`** file (or the path under **`tokengovernor/packs/`** in your project).
