# Workspace memory

Structured **project-local notes** for engineers and agents — inspired by tiered vault patterns such as [Obsidian Mind](https://github.com/breferrari/obsidian-mind), without requiring Obsidian, plugins, or hosted services.

Place **`workspace-memory/`** beside **`universal/`**, **`cursor/`**, and **`packs/`** inside your TokenGovernor folder (whether you copied **Lite** or used **`tg init`** from **Plus**).

---

## Outcomes

- **Compound context** across sessions — goals, decisions, and topic facts — without pasting the repository into chat.
- **Tiered loading:** keep a thin always-on slice; pull depth **only when the task requires it** — see **`../packs/memory/tiered-context-loading.md`** and **`../packs/memory/retrieval-first-memory.md`**.

---

## Layout

| Path | Purpose | Tier |
|------|---------|------|
| **`north-star.md`** | Current priorities, active themes, explicit non-goals — **keep short** | Often summarized at session start |
| **`_index.md`** | One-line map of notes; update when topics or decisions move | Lightweight pointer |
| **`topics/`** | One file per theme (API conventions, deploy quirks, test strategy) | On demand |
| **`decisions/`** | Lightweight decision records | On demand |
| **`sessions/`** | Optional scratch or session notes — trim or promote upward | Often ephemeral (see **Git & privacy**) |

---

## Rules for agents

1. **Never** paste the entire memory tree by default.
2. Prefer **`_index.md`** → **one** targeted file → **short** excerpts.
3. **`north-star.md`:** quote a **small** excerpt unless the task is planning or strategy.
4. If new content overlaps **`north-star.md`**, route it to **`topics/`** or **`decisions/`** and link from **`_index.md`**.

---

## Git & privacy

- Default: **track in Git** like source so the team shares the same memory surface.
- If **`sessions/`** holds rough drafts or personal notes, ignore it in **`.gitignore`**, for example:

  ```
  tokengovernor/workspace-memory/sessions/
  ```

  Adjust the path if your TokenGovernor folder uses a different name.

---

## Do not store here

Secrets, tokens, keys, customer PII, full chat logs, or full stack traces — same boundaries as **`../packs/memory/retrieval-first-memory.md`**.
