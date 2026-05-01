# Cursor — TokenGovernor project rules

Apply these in **every** Agent / Chat session for this workspace.

## Bootstrap

- Treat **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or your copy of **`universal/TOKEN_GOVERNOR_LITE.md`**) as the source of truth for core discipline.
- Other tools: see **`packs/`** (Claude, Gemini, OpenCode, OpenClaw).
- **Project memory:** if **`tokengovernor/workspace-memory/`** exists, use **`workspace-memory/README.md`** — tiered reads (`_index.md` → one topic/decision file); never dump the whole folder into chat.
- Optional **premium** coding-norm packs live in **TokenGovernor Plus** if you use it.

## Token & context discipline

- Default: **no** broad codebase search without a stated hypothesis.
- **Max ~3 file reads** before stopping to re-plan or ask for a path (unless user explicitly authorizes exploration).
- **No full log paste** — summarize errors; ask for the smallest repro snippet.
- Prefer **implementation plan** before touching more than **two** files in one task.

## Safety

- **Never** commit `.env`, `.pem`, keys, or database dumps.
- **Ask first** for: dependency install, git destructive ops, migrations, prod config, file deletes.
- **Secrets:** refuse to echo or store; redact in summaries.

## Optional: AgentOS elsewhere

If another workspace adds an **`agentos/`** tree, follow that project’s AgentOS docs—TokenGovernor OSS does not ship **`agentos/`** in this repo.
