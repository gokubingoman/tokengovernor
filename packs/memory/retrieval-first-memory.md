# Retrieval-first memory

**Goal:** Durable, useful context **without** turning memory into a junk drawer or secret vault.

---

## Store

- Architecture facts (date if they go stale)
- Stable API shapes and pointers to canonical source
- Decisions with rationale (lightweight ADR style)
- Known issues and mitigations
- **Non-secret** environment facts — service names, ports, feature-flag **names** (not secret values)

---

## Do not store

- API keys, tokens, passwords, private keys
- Entire prompts, chat logs, or stack traces
- Whole files copied “for reference”
- Customer PII or third-party confidential material

---

## Retrieval habit

Before loading “memory,” **fetch only what the current task needs**. If the project defines AgentOS **Context To Load** lists under **`agentos/`**, honor those. Do not paste an entire memory tree into chat by default.

**Tiered loading:** keep standing rules small; pull facts **on demand** — see **`tiered-context-loading.md`** (pattern related to [Obsidian Mind](https://github.com/breferrari/obsidian-mind)).

---

## Maintenance

When code and memory disagree, **update the notes or flag the drift** — do not let agents rely on obsolete architecture.
