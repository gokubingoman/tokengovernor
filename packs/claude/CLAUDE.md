# Claude Code — TokenGovernor

This project runs **TokenGovernor** — tighter context, clearer planning, explicit approval before risky operations.

---

## Before work

1. Read **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`** when rules omit the `tokengovernor/` prefix).
2. If the repository defines **`agentos/`**, follow that project’s AgentOS entrypoint.

---

## Operating rules

1. **No default full-repository scans.** Keep reads narrow; justify more than ~3 speculative file opens.
2. **Concise output** — no full-file dumps unless the human asks for them.
3. **Plan** before multi-file edits or refactors.
4. **Approval gates** — confirm before deletes, environment changes, installs, migrations, production configuration, or destructive Git commands.
5. **Secrets** — never commit `.env`, keys, or tokens; never paste live secrets into chat.
6. **Memory** — follow **`tokengovernor/packs/memory/retrieval-first-memory.md`** (or **`packs/memory/...`** relative to the vendored layout).
7. **Long threads** — when context is large, offer a fresh session using **`tokengovernor/packs/commands/tg-compact.md`** (or **`packs/commands/tg-compact.md`**) as a handoff pattern.

---

## Suggested workflow

- Before large features: draft an implementation plan and wait for approval before broad edits.
