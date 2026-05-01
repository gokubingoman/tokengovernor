# Example: before and after

Illustrates how TokenGovernor changes agent **process**, not magic.

---

## Before (high waste)

1. **You:** “Fix the bug.”
2. **Agent:** Reads many files, pastes large components, proposes a broad refactor, runs wide search, suggests dependency installs without asking.

---

## After (TokenGovernor baseline + packs)

1. **You:** “Fix the bug.”
2. **Agent:** Asks for **error text and one file path**, or reads **≤ ~3** files under a stated hypothesis.
3. **Agent:** **Plans** a minimal change, names files to touch, implements, verifies with a **small** repro.
4. **Agent:** **Does not** install dependencies or delete files without confirmation.
5. **Agent:** Offers **`tg-compact`** patterns when the thread is long.

---

## Note

Rules steer **process**. You still supply the signal (error snippet, path, or scope) that makes the task well-posed.
