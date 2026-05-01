# Staying current — TokenGovernor Lite

TokenGovernor Lite updates when the Markdown kit on the default branch (or a release tag) changes. Your project keeps whatever copy you vendor — refresh when you want upstream fixes or new packs.

---

## Refreshing your copy

1. Pull the latest **`main`** (or a **release tag**) from [TokenGovernor](https://github.com/gokubingoman/tokengovernor).
2. Merge or copy **`universal/`**, **`cursor/`**, **`packs/`**, and **`workspace-memory/`** into your vendored folder.
3. If you customized any file, diff against upstream and re-apply your changes.

Submodules: `git submodule update --remote` (or pin to tags for stability).

---

## If you use TokenGovernor Plus

Use the **`tg`** workflow and release notes from your **Plus** distribution to refresh rules and templates inside application repos.
