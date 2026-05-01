<div align="center">

<img src="docs/assets/logo.svg" width="132" height="132" alt="TokenGovernor logo" />

# TokenGovernor

**Free cost-control rules for AI coding agents.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)

[Install](INSTALL.md) · [Pair with RTK](docs/RTK_PAIRING.md) · [Security](SECURITY.md)

</div>

---

## What this is

**TokenGovernor** (this repo — **Lite**) helps AI coding agents **waste fewer tokens** through **rules and workflows**: bounded reads, plans before big edits, approval gates, and light-weight memory guidance.

- **Rules-based.** There is **no** hard runtime enforcement, license server, or hosted dashboard in this repo.
- **Multi-tool.** Works with **Claude Code**, **OpenClaw**, **Cursor**, **Gemini CLI**, **OpenCode**, and other agents — copy the Markdown you need into each tool’s config.
- **Complements output filters.** For **shell / CLI output** compression, pair with **[RTK](https://github.com/rtk-ai/rtk)** — see [docs/RTK_PAIRING.md](docs/RTK_PAIRING.md).

**TokenGovernor Plus** (separate product/repo) adds the **`tg`** CLI, polished installer, advanced rules, premium templates, industry packs, AgentOS-friendly layouts, and an update workflow. A future **Pro** / dashboard offering is **not** part of Lite.

---

## What’s in this repo

| Path | Purpose |
|------|---------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | Universal non-negotiables + low-token response shape |
| **`cursor/rules.md`** | Cursor Agent / Chat baseline |
| **`packs/`** | Claude, Gemini, OpenCode, OpenClaw, session commands, memory policy, security / approval gates, one simple example |
| **`workspace-memory/`** | Optional project-local Markdown memory (north star, topics, decisions) |

---

## Quick start

Copy this repo (or a subtree) into your application project and point your agent at **`universal/TOKEN_GOVERNOR_LITE.md`** and **`cursor/rules.md`** (or the packs for other tools). See **[INSTALL.md](INSTALL.md)** for concrete paths and a paste snippet.

---

## Upgrade to TokenGovernor Plus

**Plus** is for teams that want install automation and deeper packs — not required to benefit from Lite.

**Upgrade to TokenGovernor Plus** for:

- **`tg` CLI** — `init`, `memory-init`, `doctor`, `version`
- **One-command setup** — vendor rules into any app repo
- **Advanced rules** and curated **premium templates**
- **Industry packs**
- **AgentOS-compatible** workflows and structure
- **Update workflow** when we ship new packs and CLI behavior

**Where to get Plus:** use your **TokenGovernor Plus** distribution or repo (commercial or private channel — not stored in this public Lite tree). If you maintain Plus separately, point contributors there for CLI and template development.

---

## Documentation

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
