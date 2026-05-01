# 安装 — TokenGovernor Lite

TokenGovernor Lite 以 **Markdown 与资源文件** 形式提供，**无需**安装器。将文件夹复制到应用仓库，并按下面路径在各 AI 工具中引用。

[返回中文 README](README.md) · [English](../../INSTALL.md)

---

## 方式 A — 复制

```bash
git clone https://github.com/gokubingoman/tokengovernor.git
cp -r tokengovernor/{universal,cursor,packs,workspace-memory} /path/to/your-project/third_party/tokengovernor
```

**Cursor：** 项目规则指向 `third_party/tokengovernor/cursor/rules.md`。  
**Claude、Gemini、OpenCode、OpenClaw：** 按各产品文档打开 `packs/` 下对应文件（**规则正文为英文**）。

---

## 方式 B — Git 子模块

```bash
cd /path/to/your-project
git submodule add https://github.com/gokubingoman/tokengovernor.git third_party/tokengovernor
```

需要可复现升级时，请将子模块固定到 tag 或 commit。

---

## 推荐目录结构

常用单一目录（多为 **`tokengovernor/`**），包含：

| 目录 | 内容 |
|------|------|
| **`universal/`** | `TOKEN_GOVERNOR_LITE.md` |
| **`cursor/`** | `rules.md` |
| **`packs/`** | 工具 packs、命令、记忆与安全 |
| **`workspace-memory/`** | 分层笔记（推荐） |

Markdown 内路径默认按此结构书写。若重命名根目录，请同步修改引用。

---

## 首次会话（粘贴到智能体）

```txt
Apply TokenGovernor from tokengovernor/universal/TOKEN_GOVERNOR_LITE.md and tokengovernor/cursor/rules.md.
Use low-token discipline: no default full-repo scans; plan before multi-file edits.
```

（建议保持**英文**，与规则文件一致。）

---

## 项目记忆

使用 **`workspace-memory/`** 存放非机密的长期上下文：`north-star.md`、`_index.md`、`topics/`、`decisions/`。策略见 **`packs/memory/tiered-context-loading.md`**、**`packs/memory/retrieval-first-memory.md`**。

---

## TokenGovernor Plus

若使用 **Plus**，请按发行说明使用 **`tg` CLI**（`tg init`、`tg memory-init`、`tg doctor`）。使用 Lite **不必**安装 Plus。

---

## 排错

见 **[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)**（英文）。
