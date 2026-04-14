# GitHub Copilot CLI — Personal Tweaks

Personal configuration and custom instructions for the [GitHub Copilot CLI](https://githubnext.com/projects/copilot-cli).

## Contents

| File | Description |
|------|-------------|
| `config.json` | Copilot CLI runtime configuration (banner settings, trusted folders, logged-in accounts) |
| `copilot-instructions.md` | Custom agent instructions injected into every Copilot CLI session |

## copilot-instructions.md

Defines a **4-tier model selection and sub-agent delegation strategy** to ensure the right AI model is used for every task — avoiding over-spending premium capacity on trivial work and under-spending it on hard problems.

### Model Tiers

| Tier | Models | Use for |
|------|--------|---------|
| **Tier 1 — Architects** | `claude-opus-4.6`, `claude-opus-4.5` | Hard bugs, architecture decisions, ambiguous requirements |
| **Tier 2 — Tech Leads** | `claude-sonnet-4.6`, `gpt-5.1`, `gpt-5.2` | Daily implementation, debugging, refactoring, code review |
| **Tier 3 — Implementers** | `gpt-5.3-codex`, `gpt-5.1-codex-max`, `gpt-5.1-codex` | Mechanical code generation from clear specs |
| **Tier 4 — Executors** | `claude-haiku-4.5`, `gpt-5-mini`, `gpt-4.1` | File searches, quick edits, boilerplate, CLI commands |

### Core Principle

> Classify the task → Route to the lowest capable tier → Delegate to a sub-agent if the task is below your current model tier.

This prevents expensive models from doing cheap work and cheap models from handling risky decisions.

## config.json

Runtime settings for the Copilot CLI:

- **`banner`** — Controls when the welcome banner is shown (`"always"`)
- **`trusted_folders`** — Directories the CLI is permitted to operate in
- **`logged_in_users`** — GitHub accounts authenticated with the CLI
- **`asked_setup_terminals`** — Tracks which terminals have been configured (e.g., Windows Terminal)
