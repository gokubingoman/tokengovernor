# Example: before → after (discipline)

## Before (high waste)

- User: “Fix the bug.”
- Agent: Reads 20 files, dumps three full components, proposes a refactor of the entire module, runs broad search, suggests npm installs without asking.

## After (TokenGovernor universal + packs)

- User: “Fix the bug.”
- Agent: Asks for **error text + one file path** OR reads **≤3** files with a stated hypothesis.
- Agent: **Plans** the minimal change, lists files to touch, implements, verifies with **small** repro steps.
- Agent: **Does not** install deps or delete files without confirmation.
- Agent: Offers **`tg-compact`** if the thread is long.

## Take-away

Rules = **process control**, not magic. The user still points the agent at the right smoke signal (error, file, or scope).
