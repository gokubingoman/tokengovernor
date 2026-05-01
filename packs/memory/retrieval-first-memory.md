# Retrieval-first memory policy

**Goal:** Useful long-term context **without** turning memory into a junk drawer or secret store.

## Store

- Architecture facts (with dates if stale risk)
- Stable API shapes and links to canonical code paths
- Decisions with rationale (ADR-lite)
- Known issues and mitigations
- **Non-secret** environment facts: service names, ports, feature flags (not values)

## Do not store

- API keys, tokens, passwords, private keys
- Full prompts, full chat logs, full stack traces
- Entire files copied “for reference”
- Customer PII or proprietary third-party data

## Retrieval rule

Before loading “memory,” **retrieve** only what the current task needs (match AgentOS **Context To Load** lists when `agentos/` is present). Never paste entire `memory/` into chat by default.

**Tiered loading:** keep always-on rules small; pull facts **on demand** via search or scoped reads — see **`tiered-context-loading.md`** (pattern adapted from [Obsidian Mind](https://github.com/breferrari/obsidian-mind)).

## Refresh

When code contradicts memory, **fix memory or flag it**—do not let agents rely on ghost architecture.
