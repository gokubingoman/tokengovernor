# Install TokenGovernor (Lite)

Lite is **rules in Markdown** — no CLI in this repo. Copy files into your project (or submodule) and reference them from your agent configuration.

## Option A — Copy into your repo

From a clone of **this** repository:

```bash
git clone https://github.com/gokubingoman/tokengovernor.git
cp -r tokengovernor/{universal,cursor,packs,workspace-memory} /path/to/your-project/third_party/tokengovernor
```

Then in **Cursor**, point project rules at `third_party/tokengovernor/cursor/rules.md` (or your chosen path). For **Claude / Gemini / OpenCode / OpenClaw**, open the matching files under `packs/` and paste or wire them per that tool’s docs.

## Option B — Submodule (optional)

```bash
cd /path/to/your-project
git submodule add https://github.com/gokubingoman/tokengovernor.git third_party/tokengovernor
```

## Layout in your project

Use one folder (often **`tokengovernor/`**) containing:

- **`universal/`** — `TOKEN_GOVERNOR_LITE.md`
- **`cursor/`** — `rules.md`
- **`packs/`** — tool packs, commands, memory docs, security
- **`workspace-memory/`** — optional tiered notes; see `workspace-memory/README.md`

Paths inside the Markdown files assume this layout. If you rename the folder, adjust cross-references.

## First session (paste)

```txt
Apply TokenGovernor from tokengovernor/universal/TOKEN_GOVERNOR_LITE.md and tokengovernor/cursor/rules.md.
Use low-token discipline: no default full-repo scans; plan before multi-file edits.
```

## Pair with RTK (shell output)

TokenGovernor shapes **agent behavior**; **[RTK](https://github.com/rtk-ai/rtk)** filters **command output**. See [docs/RTK_PAIRING.md](docs/RTK_PAIRING.md).

## Optional: persistent memory

Use **`workspace-memory/`** for project-local durable notes (`north-star.md`, `_index.md`, `topics/`, `decisions/`). Discipline: **`packs/memory/tiered-context-loading.md`**, **`packs/memory/retrieval-first-memory.md`**.

## One-command install (Plus)

If you use **TokenGovernor Plus**, use the **`tg`** CLI there (`tg init`, `tg memory-init`, `tg doctor`) — not part of this Lite repo.
