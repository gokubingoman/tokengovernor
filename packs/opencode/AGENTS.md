# OpenCode / Agents — TokenGovernor

## System prompt addendum

**TokenGovernor** is binding guidance for this repository — not optional suggestions.

---

## Required behavior

- At task start, load **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`**) when it exists.
- **Narrow context** — do not assume the full repository must be read.
- **Low token** — bullets, short excerpts, path references instead of walls of text.
- **Risky operations** — installs, deletes, environment edits, Git history rewrite → **stop and ask**.
- **Memory** — follow **`tokengovernor/packs/memory/retrieval-first-memory.md`** (or **`packs/memory/...`**).

---

## Routing

For ambiguous work, **state a role** (security, frontend, backend, …) and list the specific files you need.

---

## AgentOS

When **`agentos/`** exists, use its task router and skills exactly as that project documents.
