# OpenCode / Agents — TokenGovernor

## System prompt addendum

This project uses **TokenGovernor**. Treat it as **hard guidance**, not suggestions.

## Required behavior

- Load **`tokengovernor/universal/TOKEN_GOVERNOR_LITE.md`** (or **`universal/TOKEN_GOVERNOR_LITE.md`**) at task start when available.
- **Narrow context:** do not assume you must read “the whole repo.”
- **Low token:** prefer bullets, small code excerpts, and path references over walls of text.
- **Risky ops:** installs, deletes, env changes, git history rewrite → **stop and ask**.
- **Memory:** follow **`tokengovernor/packs/memory/retrieval-first-memory.md`** (or **`packs/memory/...`**).

## Routing

For ambiguous work, **name a role** (security, frontend, backend, etc.) and state which files you need.

## Optional AgentOS

If **`agentos/`** exists in this project, use its task-router / skills as that project defines.
