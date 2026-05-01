# Approval gates

TokenGovernor cannot **block** tool calls at runtime. It **requires explicit human confirmation** before operations that often waste tokens, leak data, or damage the codebase.

---

## Confirm before proceeding

| Action | Why it matters |
|--------|----------------|
| `git reset --hard`, `git clean -fd`, force push | Irreversible or history-destructive |
| Deleting files or directories | Easy to mis-scope with automation |
| Installing packages / changing lockfiles | Supply-chain and noise risk |
| Editing `.env*`, production secrets, CI deploy keys | Credential exposure |
| Database migrations / schema drops | Data loss |
| Restarting production services | Large blast radius |
| Disabling security headers, authentication, or rate limits | Security regression |

---

## Suggested user message

```txt
Stop and ask before deletes, installs, env changes, migrations, or Git history rewrites.
```

---

## After approval

Execute the **smallest** change set that satisfies the request. If the project includes **`agentos/`** and defines memory workflows there, follow those conventions for ongoing notes.
