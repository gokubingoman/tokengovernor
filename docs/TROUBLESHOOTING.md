# Troubleshooting — TokenGovernor Lite

## Agent ignores the rules

- **Confirm the tool is loading the file.** In Cursor, rules must point at your real path (e.g. `third_party/tokengovernor/cursor/rules.md`). For Claude / Gemini / OpenCode / OpenClaw, paste or attach the correct `packs/...` file per that product’s docs.
- **Stick to one “source of truth”.** If both `universal/TOKEN_GOVERNOR_LITE.md` and `cursor/rules.md` are attached, ensure they do not contradict; the universal file is the baseline.
- **Session length.** Very long threads dilute instructions. Summarize and start a fresh session, or use `packs/commands/tg-compact.md` patterns.

## Paths break after moving the folder

Markdown uses paths like `tokengovernor/packs/...`. If you rename the root folder (e.g. `tg/`), search-and-replace in your copies or keep the name `tokengovernor/` for fewer edits.

## Submodule shows old commit

Run `git submodule update --remote` (or pin to a tag and update intentionally). Merge upstream changes into any files you customized.

## Plus vs Lite confusion

- **Lite (this repo):** copy `universal/`, `cursor/`, `packs/`, `workspace-memory/` only.
- **Plus:** `tg init` and the CLI live in the Plus repository; Lite does not ship `packages/cli/`.

## Still stuck?

Open a [GitHub issue](https://github.com/gokubingoman/tokengovernor/issues) (non-security) or see [SECURITY.md](../SECURITY.md) for vulnerability reporting.
