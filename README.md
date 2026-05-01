<div align="center">

<img src="docs/assets/logo.svg" width="132" height="132" alt="TokenGovernor logo" />

# TokenGovernor

**Token-efficient discipline for AI coding agents — rules you own.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)

[Installation](INSTALL.md) · [RTK pairing](docs/RTK_PAIRING.md) · [Security](SECURITY.md)

</div>

---

## Overview

**TokenGovernor** is a **rules kit** for software teams using AI-assisted development. It tightens how agents read context, plan work, and ask before risky operations — so you spend fewer tokens on noise and more on shipping.

**TokenGovernor Lite** (this edition) is the **open, Markdown-only** layer: copy it into your repo, wire it into Cursor, Claude Code, OpenClaw, Gemini CLI, OpenCode, or other tools, and your agents inherit the same discipline everywhere.

| You get | Details |
|---------|---------|
| **Behavioral guardrails** | Written limits on speculative reads, log dumps, and scope creep — not a hard quota engine. |
| **Cross-tool consistency** | One `tokengovernor/` folder: universal baseline, Cursor rules, and optional **packs** per IDE. |
| **Optional project memory** | **`workspace-memory/`** tiered notes (north star, topics, decisions) so context compounds without pasting the tree. |

**Shell / CLI output** is a separate concern. For filtered command output, pair with **[RTK](https://github.com/rtk-ai/rtk)** — [RTK pairing](docs/RTK_PAIRING.md).

---

## Inside the kit

| Path | Role |
|------|------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Universal baseline: non‑negotiables, approval summary, low‑token response shape. |
| **`cursor/rules.md`** | Cursor Agent / Chat rules wired to the same baseline. |
| **`packs/`** | Claude, Gemini, OpenCode, OpenClaw, session commands, memory policy, security checklist, one worked example. |
| **`workspace-memory/`** | Optional durable notes your team and agents share (see **`workspace-memory/README.md`**). |

---

## Getting started

Add TokenGovernor next to your application code and point each tool at the paths you use. **[INSTALL.md](INSTALL.md)** has copy, submodule, and first-session steps.

---

## TokenGovernor Plus

**Plus** is the full distribution: **`tg` CLI**, one-command install into app repos, extended packs (including advanced examples), benchmarks, and update workflows suited to teams that want everything in one place.

**Plus includes:**

- **`tg`** — `init`, `memory-init`, `doctor`, `version`
- **One-command layout** — drops `universal/`, `cursor/`, `packs/`, `workspace-memory/` into a target folder
- **Advanced rules and premium templates**
- **Industry-oriented packs** (where provided in your Plus edition)
- **AgentOS-friendly** structures for projects that use them
- **Release-aligned updates** for CLI and bundled templates

Access Plus through the channel where you obtained your license or distribution. The open **Lite** edition remains here for anyone who only needs the Markdown kit.

---

## Reference

- [INSTALL.md](INSTALL.md)
- [docs/RTK_PAIRING.md](docs/RTK_PAIRING.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [CHANGELOG.md](CHANGELOG.md)
- [UPGRADE.md](UPGRADE.md)
- [SECURITY.md](SECURITY.md)

---

## Contributors

<a href="https://github.com/gokubingoman/tokengovernor/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gokubingoman/tokengovernor" alt="Contributors" />
</a>

---

## License

MIT — see [LICENSE.md](LICENSE.md).
