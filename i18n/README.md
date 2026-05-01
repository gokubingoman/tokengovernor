# Internationalization (i18n)

Human-oriented documentation is available in several languages. **Agent-facing rule files** (`universal/`, `cursor/`, `packs/**/*.md`) stay in **English** so models and IDEs get one canonical wording.

| Language | Code | Hub docs |
|----------|------|----------|
| English (canonical) | `en` | [README.md](../README.md), [INSTALL.md](../INSTALL.md) |
| Español | `es` | [README](es/README.md), [INSTALL](es/INSTALL.md), [SECURITY](es/SECURITY.md), [Pack overview](es/PACKS-OVERVIEW.md) |
| 简体中文 | `zh-CN` | [README](zh-CN/README.md), [INSTALL](zh-CN/INSTALL.md), [SECURITY](zh-CN/SECURITY.md), [Pack overview](zh-CN/PACKS-OVERVIEW.md) |
| 日本語 | `ja` | [README](ja/README.md), [INSTALL](ja/INSTALL.md), [SECURITY](ja/SECURITY.md), [Pack overview](ja/PACKS-OVERVIEW.md) |

## Contributing translations

- Fix obvious errors in an existing locale via PR.
- Propose a **new** locale by copying `i18n/es/` (or another folder), translating, and adding a row above.
- Do not translate **secrets** or customer-specific examples into public PRs.

More: [CONTRIBUTING.md](../CONTRIBUTING.md).
