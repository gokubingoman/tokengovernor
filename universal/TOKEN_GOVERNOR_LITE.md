# TokenGovernor — Universal rules

Use this file when there is **no** tool-specific hook, or as a **baseline** to merge into other configs.

**Companion files in this repo:** **`cursor/rules.md`**, **`packs/`** for IDE-specific hooks, paste commands, and expanded memory/security docs; **`workspace-memory/`** for optional **project-local** durable notes when you copy this tree into your project (see **`workspace-memory/README.md`**).

## Mission

Reduce **wasted tokens**, **context rot**, and **unsafe autopilot** for AI coding agents—through **rules and discipline**. TokenGovernor does **not** enforce hard quotas; it shapes **behavior**.

## Non-negotiables

1. **No default full-repo scan.** Explore with a **hypothesis**; expand reads only with justification.
2. **Max ~3 speculative file reads** — then pause, summarize, or ask the user for the next path.
3. **Plan before multi-file or behavioral changes.**
4. **No full-file dumps** unless explicitly requested.
5. **No full logs** — extract the minimal lines (error + stack top + file).
6. **Secrets:** never write secrets to disk in plaintext in the repo; never commit `.env*`; do not echo secrets in chat.
7. **Risk gates:** confirm before deletes, installs, migrations, prod config, `git` destructive commands (see **Approval gates** below).
8. **Memory hygiene (summary):** store only non-secret architecture, decisions, APIs, known issues; **never** API keys or PII; retrieve only what the task needs—use **`workspace-memory/`** for project-local notes when present (**`workspace-memory/README.md`**); **full policy:** `packs/memory/retrieval-first-memory.md`; **tiered bootstrap:** `packs/memory/tiered-context-loading.md`.
9. **Honesty:** do not claim features this repo does not provide (e.g. hosted dashboards, license servers) unless your project actually includes them.

## Approval gates (summary)

Ask first: **`git reset --hard` / force push**, **deletes**, **package or lockfile changes**, **`.env*` / prod secrets**, **migrations / schema drops**, **prod restarts**, **disabling auth or rate limits**.

## Low-token response shape

- Short goal restatement (one line)
- Plan (bullets)
- Work (minimal diffs / snippets)
- Verification steps

## Optional: advanced coding norms

**Lite** focuses on **context, tokens, and safety**. **TokenGovernor Plus** includes additional **premium** norms and examples (e.g. extended discipline packs) you can merge into IDE/agent rules if you use Plus.

## Shell tooling

This file does **not** compress shell output. For that, pair with **[RTK](https://github.com/rtk-ai/rtk)** — see **`docs/RTK_PAIRING.md`**.

## Layout in your project

After you copy Lite into your app repo, paths are usually **`tokengovernor/universal/`**, **`tokengovernor/cursor/`**, **`tokengovernor/packs/`**, **`tokengovernor/workspace-memory/`** (or your chosen folder name). **TokenGovernor Plus** can install the same layout with **`tg init`**.
