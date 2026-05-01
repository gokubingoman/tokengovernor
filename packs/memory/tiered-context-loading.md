# Tiered context loading

**Intent:** Spend tokens on **what the task needs now**, not on material you might need someday.

Adapted from the **tiered context** model in **[Obsidian Mind](https://github.com/breferrari/obsidian-mind)** (vault discipline, optional semantic tooling). TokenGovernor does **not** bundle Obsidian, ShardMind, or QMD — the **habits** transfer: rules, memory, and code notes without dumping whole trees into the model.

---

## Layers

| Layer | What belongs | Token stance |
|-------|----------------|--------------|
| **Always-on (small)** | Project rules — **`TOKEN_GOVERNOR_LITE`**, tool rules such as `cursor/rules.md`, optional **short** excerpt from **`workspace-memory/north-star.md`**, one or two lines of **current goal** if useful | Stable, short; resist turning this into a scrapbook |
| **On-demand (targeted)** | Grep-like hits, memory lookups, doc queries, optional semantic retrieval if your stack provides it | Snippets and paths, not whole directories |
| **Triggered (minimal)** | Per-turn hints — lint summaries, “you just wrote a file — check X” nudges | Brief nudges only |
| **Rare / explicit** | Full-file reads, large dumps, entire logs | Only when **justified** or **explicitly requested** — aligns with “no full logs / no surprise full-file dumps” |

---

## Operating habits

1. **Retrieve, then read.** Prefer search or index → open **one** file or **one** region instead of walking the tree blindly (pairs with **`retrieval-first-memory.md`**).
2. **Bootstrap with excerpts.** Session-start injections (rules, prompts, hooks) should use **excerpts and listings**, not every file under **`workspace-memory/`** (see **`workspace-memory/README.md`**).
3. **Isolate heavy work.** Large audits or refactors belong in **separate sessions** or tools so they do not inflate the main thread.
4. **Semantic search is optional.** Without RAG, tiered loading still works: **narrow search**, **human path hints**, **small excerpts**.

---

## `workspace-memory/`

When TokenGovernor is present in your project you get **`tokengovernor/workspace-memory/`** (or `<target>/workspace-memory/`): **`north-star.md`**, **`_index.md`**, **`topics/`**, **`decisions/`**, optional **`sessions/`**. Conventions live in **`workspace-memory/README.md`**.

Older installs that predate the folder can add it with **`tg memory-init`** when using **TokenGovernor Plus**.

This is **plain Markdown** — no graph database or vendor hooks required.

---

## How this fits the rest of TokenGovernor

| Document | Role |
|----------|------|
| **`workspace-memory/README.md`** | Structure and agent rules for local notes |
| **`packs/memory/retrieval-first-memory.md`** | What to store / omit; retrieval-first habit |
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Speculative read caps, logs, planning |
| **`docs/RTK_PAIRING.md`** | _Optional._ Shell/CLI filtering notes — orthogonal to TokenGovernor rules |

---

## Measurement

Obsidian Mind publishes example token **targets** for **their** automation stack. Your figures depend on rule length, model, and tooling — **measure in your environment** if you need budgets. This document defines **shape**, not a guarantee.
