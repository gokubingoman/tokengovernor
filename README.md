<div align="center">

<img src="docs/assets/logo.svg" width="132" height="132" alt="TokenGovernor logo" />

# TokenGovernor

**Token-efficient discipline for AI coding agents — rules you own.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)

[Installation](INSTALL.md) · [Security](SECURITY.md) · [Languages / 语言 / 言語](i18n/README.md)

</div>

---

## Contents

- [Overview](#overview)
- [Who it is for](#who-it-is-for)
- [Inside the kit](#inside-the-kit)
- [Getting started](#getting-started)
- [Documentation map](#documentation-map)
- [TokenGovernor Plus](#tokengovernor-plus)
- [Contributors](#contributors)
- [License](#license)

---

## Overview

**TokenGovernor** is a **rules kit** for software teams using AI-assisted development. It tightens how agents read context, plan work, and ask before risky operations — so you spend fewer tokens on noise and more on shipping.

**TokenGovernor Lite** (this edition) is the **open, Markdown-only** layer: copy it into your repo, wire it into Cursor, Claude Code, OpenClaw, Gemini CLI, OpenCode, or other tools, and your agents inherit the same discipline everywhere.

| You get | Details |
|---------|---------|
| **Behavioral guardrails** | Written limits on speculative reads, log dumps, and scope creep — not a hard quota engine. |
| **Cross-tool consistency** | One `tokengovernor/` folder: universal baseline, Cursor rules, and optional **packs** per IDE. |
| **Optional project memory** | **`workspace-memory/`** tiered notes (north star, topics, decisions) so context compounds without pasting the tree. |

---

## Who it is for

- Teams that want **predictable agent behavior** across Cursor, Claude, Gemini, OpenCode, OpenClaw, or similar.
- Projects where **context hygiene** (no default full-repo scans, no full log dumps) matters for cost and reviewability.
- Users who prefer **owning rules as files** in Git over a hosted control plane.

---

## Inside the kit

| Path | Role |
|------|------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Universal baseline: non‑negotiables, approval summary, low‑token response shape. |
| **`cursor/rules.md`** | Cursor Agent / Chat rules wired to the same baseline. |
| **`packs/`** | Claude, Gemini, OpenCode, OpenClaw, session commands, memory policy, security checklist, one worked example. |
| **`workspace-memory/`** | Optional durable notes your team and agents share (see **`workspace-memory/README.md`**). |
| **`docs/`** | [Glossary](docs/GLOSSARY.md), [Troubleshooting](docs/TROUBLESHOOTING.md). |
| **`i18n/`** | [Translated hub docs](i18n/README.md) (ES / zh-CN / JA); **packs stay English** for LLM use. |

---

## Getting started

Add TokenGovernor next to your application code and point each tool at the paths you use.

1. Follow **[INSTALL.md](INSTALL.md)** (copy, submodule, layout, first-session paste).
2. If something misbehaves, see **[docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md)**.
3. For terminology, see **[docs/GLOSSARY.md](docs/GLOSSARY.md)**.

---

## Documentation map

| Document | Purpose |
|----------|---------|
| [INSTALL.md](INSTALL.md) | Install and layout |
| [UPGRADE.md](UPGRADE.md) | Staying current |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [CHANGELOG.md](CHANGELOG.md) | Release notes |
| [SECURITY.md](SECURITY.md) | Responsible disclosure |
| [docs/GLOSSARY.md](docs/GLOSSARY.md) | Terms |
| [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Common issues |
| [i18n/README.md](i18n/README.md) | Languages index |

---

## TokenGovernor Plus

**Plus** (**from $9/month**) is the full distribution—same behavioral baseline as Lite, packaged for teams that want automation and depth:

| Lite (this repo) | Plus |
|------------------|------|
| Copy or submodule Markdown | **`tg` CLI** — `init`, `memory-init`, `doctor`, `version` |
| Baseline `packs/` | **Extended `packs/`** — premium-style norms, longer examples |
| No installer in-tree | **One-command layout** into app repos via **`@tokengovernor/cli`** |
| — | **Benchmarks** and methodology docs |

Subscribe or purchase through the channel documented on **[TokenGovernor Plus](https://github.com/gokubingoman/tokengovernor-plus)** (see INSTALL). The open **Lite** edition stays here for anyone who only needs the Markdown kit for free.

---

## Contributors

<a href="https://github.com/gokubingoman/tokengovernor/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gokubingoman/tokengovernor" alt="Contributors" />
</a>

---

## License

MIT — see [LICENSE.md](LICENSE.md).
