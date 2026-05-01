# TokenGovernor — Universal baseline

Use this file as the **default policy** when a tool has no native hook, or merge excerpts into tool-specific configs.

**Shipped next to:** **`cursor/rules.md`**, **`packs/`** (IDE extensions, commands, memory and security detail), and optional **`workspace-memory/`** for project-local notes — see **`workspace-memory/README.md`**.

---

## Mission

Cut **wasted tokens**, **stale context**, and **unsafe autopilot** in AI-assisted development. TokenGovernor shapes **behavior**; it does not impose hard token quotas or remote enforcement.

---

## Non-negotiables

1. **No default full-repo scan.** Start from a **hypothesis**; widen reads only with a short justification.
2. **Cap speculative reads** at roughly **three files**, then pause, summarize, or ask which path to open next.
3. **Plan** before multi-file or behavior-changing edits.
4. **No full-file dumps** unless the human explicitly asks for them.
5. **No full logs** — pull the smallest slice: error line, top of stack, file path.
6. **Secrets:** never write secrets into the repo in plain text; never commit `.env*`; never repeat live secrets in chat.
7. **Risk gates:** confirm before deletes, installs, migrations, production config, or destructive Git operations (see **Approval gates** below).
8. **Memory:** store only non-secret architecture facts, decisions, APIs, and known issues — never API keys or PII. Retrieve **just what the task needs**; see **`workspace-memory/README.md`**, **`packs/memory/retrieval-first-memory.md`**, **`packs/memory/tiered-context-loading.md`**.
9. **Accuracy:** do not claim capabilities your project does not have (hosted dashboards, license servers, telemetry products, and so on).

---

## Approval gates (summary)

Confirm before: **`git reset --hard`**, **force push**, **deletes**, **dependency or lockfile changes**, **`.env*` / production secrets**, **schema drops**, **production restarts**, **weakening auth or rate limits**.

---

## Low-token response shape

- One-line goal restatement  
- Short plan (bullets)  
- Minimal diffs / snippets  
- Concrete verification steps  

---

## Optional: deeper coding norms

This baseline focuses on **context, tokens, and safety**. **TokenGovernor Plus** adds optional **premium** norms and longer-form examples you can merge into tool rules when you use that edition.

---

## Shell output

This baseline does **not** install or enforce shell/terminal filters. That is a separate layer. If you care about it, your team can document or adopt tooling as needed — **`docs/RTK_PAIRING.md`** in this kit is an **optional** pointer, not part of the rule set.

---

## Paths in your repository

After you vendor TokenGovernor, you typically have **`tokengovernor/universal/`**, **`tokengovernor/cursor/`**, **`tokengovernor/packs/`**, and **`tokengovernor/workspace-memory/`** (folder names may vary). **TokenGovernor Plus** can lay down the same structure with **`tg init`**.
