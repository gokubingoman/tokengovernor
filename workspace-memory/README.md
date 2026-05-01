# Workspace memory

**Project-local notes** for humans and AI agents — inspired by tiered “vault” patterns (e.g. [Obsidian Mind](https://github.com/breferrari/obsidian-mind)), without requiring Obsidian or extra services.

Live beside **`universal/`**, **`cursor/`**, and **`packs/`** under your **`tokengovernor/`** folder (or whatever folder name you used when copying Lite / running **`tg init`** in Plus).

## Job-to-be-done

- **Compound context** across sessions (goals, decisions, topic facts) without pasting the whole repo into chat.
- **Tiered loading**: keep a tiny slice always relevant; pull depth **only when needed** — see **`../packs/memory/tiered-context-loading.md`** and **`../packs/memory/retrieval-first-memory.md`**.

## Layout

| Path | Purpose | Tier |
|------|---------|------|
| **`north-star.md`** | Current priorities, active themes, non-goals — **keep short** | Often summarized / excerpted at session start |
| **`_index.md`** | Map of what lives where (one line per note); update when you add topics/decisions | Lightweight pointer |
| **`topics/`** | One file per theme (API conventions, deployment quirks, “how we test”) | On-demand reads |
| **`decisions/`** | ADR-lite / decision records | On-demand reads |
| **`sessions/`** | Optional session summaries or scratch — trim or delete when promoted | Ephemeral (often **gitignored** — see below) |

## Rules for agents

1. **Never paste this entire tree** into context by default.
2. **Prefer** `_index.md` → open **one** targeted file → quote minimal excerpts.
3. **North star**: at most a **small excerpt** unless the task is planning/strategy.
4. When something belongs in memory **and** duplicates `north-star.md`, prefer **`topics/`** or **`decisions/`** and link from `_index.md`.

## Git & privacy

- Default expectation: **git-tracked** like code so the team shares memory.
- If **`sessions/`** holds rough dumps or personal notes, add to **`.gitignore`**:

  ```
  tokengovernor/workspace-memory/sessions/
  ```

  (Adjust path if your TokenGovernor folder name differs.)

## Do **not** store here

Secrets, tokens, keys, customer PII, full chat logs, full stack traces — same policy as **`../packs/memory/retrieval-first-memory.md`**.
