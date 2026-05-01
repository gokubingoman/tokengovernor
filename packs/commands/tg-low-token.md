# Session command: low-token answers

Use when replies are growing **long** or you want **minimal** assistant output.

---

## Paste into the agent

```txt
TokenGovernor low-token mode:
- Stay under fifteen lines unless I ask for more.
- No code blocks longer than forty lines.
- No file dumps — use path:line references.
- If something is unclear, ask exactly one clarifying question.
```

---

## When it helps

- Tight feedback loops, small edits, yes/no decisions.
- You already know the target file and need a surgical change.
