# Installation — TokenGovernor Lite

TokenGovernor Lite ships as **Markdown and assets** — no installer required. Choose a layout, copy the folder into your application repository, and connect each AI tool to the paths below.

---

## Option A — Copy

```bash
git clone https://github.com/gokubingoman/tokengovernor.git
cp -r tokengovernor/{universal,cursor,packs,workspace-memory} /path/to/your-project/third_party/tokengovernor
```

**Cursor:** set project rules to `third_party/tokengovernor/cursor/rules.md` (or your path).  
**Claude, Gemini, OpenCode, OpenClaw:** open the matching files under `packs/` and attach or paste per that tool’s documentation.

---

## Option B — Git submodule

```bash
cd /path/to/your-project
git submodule add https://github.com/gokubingoman/tokengovernor.git third_party/tokengovernor
```

Pin the submodule to a tag or commit when you want reproducible upgrades.

---

## Recommended layout

Keep a single directory (often **`tokengovernor/`**) containing:

| Directory | Contents |
|-----------|----------|
| **`universal/`** | `TOKEN_GOVERNOR_LITE.md` |
| **`cursor/`** | `rules.md` |
| **`packs/`** | Tool packs, commands, memory, security |
| **`workspace-memory/`** | Tiered notes (optional but recommended) |

Paths in the Markdown assume this structure. If you rename the folder, update cross-references accordingly.

---

## First session (paste into your agent)

```txt
Apply TokenGovernor from tokengovernor/universal/TOKEN_GOVERNOR_LITE.md and tokengovernor/cursor/rules.md.
Use low-token discipline: no default full-repo scans; plan before multi-file edits.
```

---

## RTK (command output)

TokenGovernor shapes **how the model reasons**; **[RTK](https://github.com/rtk-ai/rtk)** narrows **what reaches the model** from the shell. They stack cleanly — see [docs/RTK_PAIRING.md](docs/RTK_PAIRING.md).

---

## Project memory

Use **`workspace-memory/`** for durable, non-secret context: `north-star.md`, `_index.md`, `topics/`, `decisions/`. Policy and loading order: **`packs/memory/tiered-context-loading.md`**, **`packs/memory/retrieval-first-memory.md`**.

---

## TokenGovernor Plus

If you use **Plus**, install with the **`tg`** CLI (`tg init`, `tg memory-init`, `tg doctor`) from your Plus distribution. Plus is not required to use Lite.
