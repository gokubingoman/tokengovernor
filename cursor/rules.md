# Cursor — TokenGovernor

Apply these directives in **every** Agent / Chat session tied to this codebase.

---

## Load order

1. **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`** if the `tokengovernor/` prefix is omitted).
2. Tool-specific material in **`packs/`** (Claude, Gemini, OpenCode, OpenClaw) when the same project uses those agents.
3. **Project memory:** if **`tokengovernor/workspace-memory/`** exists, honor **`workspace-memory/README.md`** — read **`_index.md`**, then **one** topic or decision file; never load the entire tree into context by default.
4. **Extended coding norms** (assumptions, minimal scope, surgical edits, verifiable goals): available in **TokenGovernor Plus** packs when you use that edition — merge into project rules there if you want them always on.

---

## Context discipline

- **No** broad codebase search without a stated hypothesis.
- **~Three speculative file reads**, then re-plan or ask for the next path unless the human expands scope.
- **No full log paste** — summarize; request the smallest failing excerpt.
- Prefer a short **implementation plan** before changing more than **two** files in one task.

---

## Safety

- **Never** commit `.env`, `.pem`, private keys, or database dumps.
- **Ask first** before: dependency installs, destructive Git operations, migrations, production configuration, or file deletes.
- **Secrets:** do not echo or persist; redact in summaries.

---

## AgentOS

If the project includes an **`agentos/`** tree, follow that project’s AgentOS entrypoints. **TokenGovernor Lite** does not ship **`agentos/`** here.
