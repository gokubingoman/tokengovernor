# Approval gates (Plus pack)

TokenGovernor cannot **block** dangerous actions at runtime. It **requires explicit human approval** for operations that commonly waste tokens, leak data, or damage the repo.

## Always require confirmation

| Action | Why |
|--------|-----|
| `git reset --hard`, `git clean -fd`, force push | Irreversible / destructive |
| Deleting files or directories | Often wrong-scope for AI |
| Installing packages / changing lockfiles | Supply chain + noise |
| Editing `.env*`, production secrets, CI deploy keys | Credential risk |
| DB migrations / schema drops | Data loss |
| Restarting production services | Blast radius |
| Disabling security headers, auth checks, or rate limits | Security regression |

## Suggested prompt (user says)

```txt
Stop and ask before deletes, installs, env changes, migrations, or git history rewrite.
```

## After approval

Proceed with **minimal** change set; **Plus** or **Pro** workspaces with **`agentos/`** use `agentos/memory/` for ongoing notes.
