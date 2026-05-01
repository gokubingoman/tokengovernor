# TokenGovernor + RTK

**TokenGovernor** = **rules** (how the agent behaves: bounded reads, plans, approval gates).  
**[RTK](https://github.com/rtk-ai/rtk)** = **CLI proxy** (compresses `git status`, tests, etc., before output hits the model).

They solve different layers. Using both is reasonable:

1. Install **RTK** and run `rtk init` for your agent (see RTK docs).
2. Install **TokenGovernor** (`tg init` or copy `universal/`, `cursor/`, `packs/`).

RTK’s bash hook does **not** rewrite IDE-native tools like `Read` / `Grep` in some agents—RTK documents that; use shell commands or explicit `rtk …` where you want compression.

## Order of operations

- Either order works. Most teams: **RTK first** (shell), then **TokenGovernor** (project rules file).

## Honesty

Do not promise RTK-style “60–90% token savings” for TokenGovernor alone. For measurement and filtered command output, point people at **RTK**.
