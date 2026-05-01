# インストール — TokenGovernor Lite

TokenGovernor Lite は **Markdown とアセット**として提供され、**インストーラは不要**です。アプリケーションリポジトリにフォルダをコピーし、各 AI ツールから下記パスを参照します。

[日本語 README に戻る](README.md) · [English](../../INSTALL.md)

---

## 方法 A — コピー

```bash
git clone https://github.com/gokubingoman/tokengovernor.git
cp -r tokengovernor/{universal,cursor,packs,workspace-memory} /path/to/your-project/third_party/tokengovernor
```

**Cursor:** プロジェクトルールを `third_party/tokengovernor/cursor/rules.md` に。  
**Claude、Gemini、OpenCode、OpenClaw:** 各製品のドキュメントに従い `packs/` 内の該当ファイルを開く（**ルール本文は英語**）。

---

## 方法 B — Git サブモジュール

```bash
cd /path/to/your-project
git submodule add https://github.com/gokubingoman/tokengovernor.git third_party/tokengovernor
```

再現性のある更新のため、サブモジュールをタグまたはコミットに固定してください。

---

## 推奨レイアウト

多くの場合、**`tokengovernor/`** という単一ディレクトリに以下を含めます。

| ディレクトリ | 内容 |
|--------------|------|
| **`universal/`** | `TOKEN_GOVERNOR_LITE.md` |
| **`cursor/`** | `rules.md` |
| **`packs/`** | ツール packs、コマンド、メモリ、セキュリティ |
| **`workspace-memory/`** | 階層メモ（推奨） |

Markdown 内のパスはこの構造を前提にしています。ルート名を変える場合は相互参照を更新してください。

---

## 初回セッション（エージェントに貼り付け）

```txt
Apply TokenGovernor from tokengovernor/universal/TOKEN_GOVERNOR_LITE.md and tokengovernor/cursor/rules.md.
Use low-token discipline: no default full-repo scans; plan before multi-file edits.
```

（ルールファイルとの整合のため**英語のまま**推奨。）

---

## プロジェクトメモリ

**`workspace-memory/`** に機密でない長期コンテキストを置きます：`north-star.md`、`_index.md`、`topics/`、`decisions/`。方針は **`packs/memory/tiered-context-loading.md`**、**`packs/memory/retrieval-first-memory.md`**。

---

## TokenGovernor Plus

**Plus** を使う場合は、配布元の手順に従い **`tg` CLI**（`tg init`、`tg memory-init`、`tg doctor`）を利用します。Lite 単体では Plus は**不要**です。

---

## トラブルシュート

**[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)**（英語）を参照してください。
