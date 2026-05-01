<div align="center">

<img src="../../docs/assets/logo.svg" width="132" height="132" alt="TokenGovernor logo" />

# TokenGovernor

**面向 AI 编程助手的高效 token 纪律 —— 规则由你掌控。**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](../../LICENSE.md)

[英文 README](../../README.md) · [安装](INSTALL.md) · [安全](SECURITY.md) · [语言索引](../README.md)

</div>

---

## 目录

- [概述](#概述)
- [适用对象](#适用对象)
- [仓库里有什么](#仓库里有什么)
- [上手](#上手)
- [文档索引](#文档索引)
- [TokenGovernor Plus](#tokengovernor-plus)

---

## 概述

**TokenGovernor** 是一套面向**使用 AI 辅助开发**团队的**规则套件**，约束智能体如何读取上下文、规划工作，以及在风险操作前征求确认——减少浪费在噪声上的 token，把容量留给交付。

**TokenGovernor Lite**（本仓库）是**开源、纯 Markdown**的一层：复制到你的仓库，接入 Cursor、Claude Code、OpenClaw、Gemini CLI、OpenCode 等工具，即可在多工具间保持一致的纪律。

| 你能得到 | 说明 |
|----------|------|
| **行为护栏** | 对随意扫库、整段日志、范围蔓延等的书面约束——不是硬性配额引擎。 |
| **跨工具一致** | 一个 `tokengovernor/` 目录：通用基线、Cursor 规则与各 **packs**。 |
| **可选项目记忆** | **`workspace-memory/`** 分层笔记（北极星、主题、决策）。 |

**说明：** 模型直接读取的规则文件（`universal/`、`cursor/`、`packs/`）默认使用**英文**以便与多数模型/工具对齐；**`i18n/`** 下的内容主要供**人**阅读。

---

## 适用对象

- 希望在 Cursor、Claude、Gemini、OpenCode、OpenClaw 等之间保持**可预期智能体行为**的团队。
- 重视**上下文卫生**（禁止默认全库扫描、禁止整段日志粘贴等）以降低费用与审阅成本的用户。
- 倾向于在 Git 中以**文件形式拥有规则**，而非依赖托管控制台的用户。

---

## 仓库里有什么

| 路径 | 作用 |
|------|------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | 通用基线：底线规则、审批摘要、低 token 回复结构。 |
| **`cursor/rules.md`** | 与基线一致的 Cursor 规则。 |
| **`packs/`** | 各工具规则、会话命令、记忆策略、安全检查、示例等。 |
| **`workspace-memory/`** | 可选的持久笔记（见 [README](../../workspace-memory/README.md)）。 |
| **`docs/`** | [术语表](../../docs/GLOSSARY.md)、[排错](../../docs/TROUBLESHOOTING.md)（英文）。 |

中文 **`packs/`** 导览（给人看）：[PACKS-OVERVIEW.md](PACKS-OVERVIEW.md)。

---

## 上手

1. 阅读 **[INSTALL.md](INSTALL.md)**（拷贝、子模块、目录结构与首会话粘贴语）。
2. 遇到问题见 **[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)**（英文）。
3. 术语见 **[docs/GLOSSARY.md](../../docs/GLOSSARY.md)**（英文）。

---

## 文档索引

| 文档 | 用途 |
|------|------|
| [INSTALL.md](INSTALL.md) | 安装 |
| [UPGRADE.md](../../UPGRADE.md) | 升级（英文） |
| [CONTRIBUTING.md](../../CONTRIBUTING.md) | 贡献（英文） |
| [CHANGELOG.md](../../CHANGELOG.md) | 变更（英文） |
| [SECURITY.md](SECURITY.md) | 漏洞披露 |

---

## TokenGovernor Plus

**Plus**（**$9/月**起）在相同行为基线上提供 **`tg` CLI**、扩展 packs 与基准测试等。详见 **[TokenGovernor Plus](https://github.com/gokubingoman/tokengovernor-plus)**。

---

## 许可证

MIT — 见 [LICENSE.md](../../LICENSE.md)。
