# Glossary

Terms used across TokenGovernor documentation.

| Term | Meaning |
|------|---------|
| **Lite** | This open repository: Markdown rules, no in-tree CLI. |
| **Plus** | The full distribution ([`tokengovernor-plus`](https://github.com/gokubingoman/tokengovernor-plus)): CLI, extended packs, benchmarks. |
| **Universal baseline** | `universal/TOKEN_GOVERNOR_LITE.md` — default discipline: reads, plans, logs, secrets, approvals. |
| **Pack** | A Markdown file (or folder) under `packs/` for a specific tool or topic (e.g. Claude, memory). |
| **Workspace memory** | `workspace-memory/` — tiered project notes agents and humans read on demand. |
| **Approval gate** | A class of operations (deletes, installs, prod config, etc.) where the agent should confirm with a human first. |
| **Tiered loading** | Keeping always-on context small; pulling deeper notes only when the task needs them. |
| **Vendored / installed** | Copying the `tokengovernor/` tree into an application repository (manually, submodule, or via Plus `tg init`). |

Canonical **rules for models** are in English under `universal/`, `cursor/`, and `packs/` — see [i18n/README.md](../i18n/README.md) for human documentation in other languages.
