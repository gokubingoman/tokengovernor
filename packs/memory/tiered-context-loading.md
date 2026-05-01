# Tiered context loading

**Goal:** Spend tokens on **what the task needs now**, not on dumping everything you might someday need.

This pattern is adapted from the **tiered context** idea described in **[Obsidian Mind](https://github.com/breferrari/obsidian-mind)** (vault + hooks + optional QMD semantic search). TokenGovernor does **not** ship Obsidian, ShardMind, or QMD — but the **discipline** transfers to any repo: rules + memory + codebase notes without pasting whole trees into the model.

## Tiers (generic coding agent)

| Tier | What belongs here | Token stance |
|------|-------------------|--------------|
| **Always (small)** | Project rules: **`TOKEN_GOVERNOR_LITE`**, tool rules (`cursor/rules.md`, etc.), optionally a **short excerpt** from **`workspace-memory/north-star.md`**, 1–2 lines of **current goal** if needed | Keep stable and short; avoid stuffing “everything useful” here |
| **On-demand (targeted)** | Answers from **search**: grep-like finds, memory lookups, doc/query tools, optional **semantic** retrieval if your stack has it | Pull **snippets + paths**, not whole directories |
| **Triggered (tiny)** | Per-turn hints: classification nudges, lint summaries, “you just wrote a file — validate frontmatter” style checks | Keep hints **brief**; no transcripts |
| **Rare / explicit** | Full-file reads, large dumps, whole logs | Only when **justified** or **user-requested** — matches Lite’s “no full logs / no full-file dumps by default” |

## Operational rules

1. **Retrieve, then read.** Prefer search/list/index → open **one** file or **one** region over scanning trees blindly (pairs with **`retrieval-first-memory.md`**).
2. **Bootstrap discipline.** If you inject “session start” context (Cursor rules, custom prompts, hooks), use **excerpts + file/index listings**, not full note bodies or dumping all of **`workspace-memory/`** (see **`workspace-memory/README.md`** after `tg init`).
3. **Isolate heavy work.** Long audits or big transforms belong in **separate sub-sessions** or tools so they don’t bloat the main thread — same *effect* as Obsidian Mind’s subagents, without requiring their stack.
4. **Semantic search is optional.** If you don’t run QMD/RAG, tiered loading still works: **narrow grep**, **path hints from the user**, and **small excerpts**.

## `workspace-memory/` (ships with `tg init`)

New installs get **`tokengovernor/workspace-memory/`** (or `<target>/workspace-memory/`): a minimal **project-local** note tree (`north-star.md`, `_index.md`, `topics/`, `decisions/`, optional `sessions/`). Read **`workspace-memory/README.md`** for conventions.

Existing repos predating this folder can run **`tg memory-init`** once.

This is **not** Obsidian — no graph DB, no hooks — just Markdown + the same tiered habits.

## Relation to other TokenGovernor docs

| Doc | Role |
|-----|------|
| **`workspace-memory/README.md`** | Layout and agent rules for project-local notes |
| **`packs/memory/retrieval-first-memory.md`** | What to store / not store; retrieval-first rule |
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Hard caps: speculative reads, logs, plans |
| **`docs/RTK_PAIRING.md`** | Shell **output** compression — orthogonal layer |

## Honesty

Obsidian Mind’s README cites concrete token **targets** for *their* hooks + vault (e.g. ~2K “always” band). Your numbers depend on rules length, model, and tooling — **measure locally** if you need budgets; this file describes **shape**, not a quota guarantee.
