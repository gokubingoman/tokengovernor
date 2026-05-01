<div align="center">

<img src="../../docs/assets/logo.svg" width="132" height="132" alt="TokenGovernor logo" />

# TokenGovernor

**AI コーディングエージェントのトークン効率な規律 — ルールはあなたの手元に。**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](../../LICENSE.md)

[English README](../../README.md) · [インストール](INSTALL.md) · [セキュリティ](SECURITY.md) · [言語一覧](../README.md)

</div>

---

## 目次

- [概要](#概要)
- [対象](#対象)
- [キットの内容](#キットの内容)
- [はじめに](#はじめに)
- [ドキュメント一覧](#ドキュメント一覧)
- [TokenGovernor Plus](#tokengovernor-plus)

---

## 概要

**TokenGovernor** は、**AI アシスト開発**を行うチーム向けの**ルールキット**です。エージェントがコンテキストをどう読むか、どう計画し、リスクの高い操作の前に確認を取るかを締めます — ノイズにトークンを使わず、成果に回します。

**TokenGovernor Lite**（本リポジトリ）は**オープンで Markdown のみ**の層です。リポジトリにコピーし、Cursor、Claude Code、OpenClaw、Gemini CLI、OpenCode などに配線すれば、同じ規律を共有できます。

| 得られるもの | 内容 |
|--------------|------|
| **行動ガードレール** | 思いつき読み取り・ログ全貼り・スコープ漂流などへの言及上の制限 — ハードクォータではありません。 |
| **複数ツールでの一貫性** | `tokengovernor/` 一枚岩：ユニバーサル baseline、Cursor ルール、IDE 別 **packs**。 |
| **任意のプロジェクトメモリ** | **`workspace-memory/`** 階層メモ（ノーススター、トピック、決定）。 |

**重要:** モデルが読むルール（`universal/`、`cursor/`、`packs/`）は慣例として**英語**です。**`i18n/`** は**人間向け**のドキュメントです。

---

## 対象

- Cursor、Claude、Gemini、OpenCode、OpenClaw などで**エージェント挙動を揃えたい**チーム。
- **コンテキスト衛生**（デフォルトでの全リポジトリ走査禁止、全ログ貼り付け禁止など）をコストとレビューの両面で重視するプロジェクト。
- ホスト型のコントロールプレーンより **Git 上のファイルとしてルールを所有したい**ユーザー。

---

## キットの内容

| パス | 役割 |
|------|------|
| **`universal/TOKEN_GOVERNOR_LITE.md`** | ユニバーサル baseline：非交渉事項、承認の要約、低トークン応答の形。 |
| **`cursor/rules.md`** | Cursor 向けルール（baseline と整合）。 |
| **`packs/`** | ツール別ルール、セッションコマンド、メモリ方針、セキュリティ、例。 |
| **`workspace-memory/`** | 任意の永続メモ（[README](../../workspace-memory/README.md)）。 |
| **`docs/`** | [用語集](../../docs/GLOSSARY.md)、[トラブルシュート](../../docs/TROUBLESHOOTING.md)（英語）。 |

**`packs/`** の人向け概要（日本語）：[PACKS-OVERVIEW.md](PACKS-OVERVIEW.md)。

---

## はじめに

1. **[INSTALL.md](INSTALL.md)** に従う（コピー、サブモジュール、レイアウト、初回セッション用テキスト）。
2. 問題があれば **[docs/TROUBLESHOOTING.md](../../docs/TROUBLESHOOTING.md)**（英語）。
3. 用語は **[docs/GLOSSARY.md](../../docs/GLOSSARY.md)**（英語）。

---

## ドキュメント一覧

| 文書 | 用途 |
|------|------|
| [INSTALL.md](INSTALL.md) | インストール |
| [UPGRADE.md](../../UPGRADE.md) | 更新（英語） |
| [CONTRIBUTING.md](../../CONTRIBUTING.md) | コントリビューション（英語） |
| [CHANGELOG.md](../../CHANGELOG.md) | 変更履歴（英語） |
| [SECURITY.md](SECURITY.md) | 脆弱性開示 |

---

## TokenGovernor Plus

**Plus**（**月額 $9〜**）は同じ行動 baseline に **`tg` CLI**、拡張 packs、ベンチマークなどを提供します。詳細は **[TokenGovernor Plus](https://github.com/gokubingoman/tokengovernor-plus)** を参照してください。

---

## ライセンス

MIT — [LICENSE.md](../../LICENSE.md)。
