# Claude Code — TokenGovernor

You are working in a project that uses **TokenGovernor** for cost and context discipline.

## Before work

1. Prefer **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`** if you copied rules without the folder prefix).
2. Optional: if this repo adds **`agentos/`** elsewhere, follow that project’s AgentOS entrypoint.

## Operating rules

1. **No default full-repo scans.** Open files narrowly; justify more than ~3 speculative reads.
2. **Concise output** — no full-file dumps unless explicitly requested.
3. **Plan before multi-file edits** or refactors.
4. **Approval gates** — ask before: deletes, env changes, installs, migrations, production config, destructive git ops.
5. **Secrets** — never commit `.env`, keys, tokens; never paste live secrets into chat.
6. **Memory** — follow **`tokengovernor/packs/memory/retrieval-first-memory.md`** (or **`packs/memory/...`** relative to your layout).
7. **Compact sessions** — when context is huge, suggest a fresh session and use **`tokengovernor/packs/commands/tg-compact.md`** patterns.

## Suggested slash behaviors

- Before big features: produce an implementation plan; wait for approval.
