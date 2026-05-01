# TokenGovernor and RTK

Two layers, one workflow:

| Layer | Role |
|-------|------|
| **TokenGovernor** | **Rules** — how the agent explores, plans, and asks before risky steps. |
| **[RTK](https://github.com/rtk-ai/rtk)** | **Shell proxy** — narrows `git`, test, and build output before it reaches the model. |

They address different problems and stack cleanly.

---

## Setup

1. Install **RTK** and run `rtk init` for your environment (see RTK’s documentation).
2. Add **TokenGovernor** to your project — copy **`universal/`**, **`cursor/`**, **`packs/`** (Lite), or run **`tg init`** from **TokenGovernor Plus**.

RTK’s shell hook does not rewrite IDE-native tools such as inline **Read** / **Grep** in some products. Use shell commands or explicit `rtk …` where you want output filtered.

---

## Order

Either order works. Many teams enable **RTK** first (command line), then wire **TokenGovernor** (project rules).

---

## Expectations

TokenGovernor does not duplicate RTK’s measured shell compression. For **token estimates** tied to filtered command output, rely on **RTK**’s documentation and tooling.
