# Optional: shell / CLI output

TokenGovernor is **Markdown rules** for agent behavior. It does **not** ship a shell proxy.

Some teams also want **less raw `git`, test, or build output** in the model. That is a **different layer**.

**[RTK](https://github.com/rtk-ai/rtk)** is one open tool for filtered CLI output. Use it only if it fits your stack — it is **not** a TokenGovernor dependency.

- Install and configure RTK from **its** documentation.
- RTK hooks the shell; TokenGovernor hooks agent instructions. Either order is fine.
- IDE-native **Read** / **Grep** (and similar) are not the same as shell piping — RTK’s docs explain limits.

For expectations and savings claims, rely on **RTK**’s own materials, not TokenGovernor.
