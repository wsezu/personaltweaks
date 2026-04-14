# Personal Tweaks

A collection of personal configurations, themes, scripts, and infrastructure-as-code templates gathered over the years — covering terminal customisation, AI tooling, scripting, and cloud infrastructure across multiple operating systems.

## Repository Structure

```
Personal Tweaks/
├── GitHub Copilot CLI/     # Copilot CLI runtime config & custom agent instructions
├── IaC/
│   ├── Bicep/              # Azure Bicep templates (coming soon)
│   └── Terraform/          # Terraform configurations (coming soon)
├── Oh-my-posh/
│   └── Themes/             # Custom Oh My Posh prompt themes (.omp.json)
└── Scripting/
    ├── PowerShell/         # PowerShell scripts (coming soon)
    └── Python/             # Python scripts (coming soon)
```

---

## GitHub Copilot CLI

> 📁 [`GitHub Copilot CLI/`](./GitHub%20Copilot%20CLI/README.md)

Runtime configuration and custom instructions for the [GitHub Copilot CLI](https://githubnext.com/projects/copilot-cli).

| File | Purpose |
|------|---------|
| `config.json` | CLI settings: banner behaviour, trusted folders, logged-in GitHub accounts |
| `copilot-instructions.md` | Custom agent instructions injected into every session — defines a 4-tier model selection and sub-agent delegation strategy to right-size AI model usage per task |

The instruction file establishes four tiers:

| Tier | Models | Use for |
|------|--------|---------|
| Tier 1 — Architects | `claude-opus-4.6` | Hard bugs, architecture, ambiguous requirements |
| Tier 2 — Tech Leads | `claude-sonnet-4.6`, `gpt-5.1` | Daily implementation, debugging, code review |
| Tier 3 — Implementers | `gpt-5.3-codex`, `gpt-5.1-codex` | Mechanical code generation from clear specs |
| Tier 4 — Executors | `claude-haiku-4.5`, `gpt-5-mini` | File searches, quick edits, boilerplate, CLI commands |

---

## Oh My Posh — Themes

> 📁 [`Oh-my-posh/`](./Oh-my-posh/README.md)

Custom [Oh My Posh](https://ohmyposh.dev/) prompt themes built around a consistent powerline style with Git awareness, GitHub Copilot integration, and cross-platform OS icons.

| Theme | Highlights |
|-------|-----------|
| `wsezu.full` | Two-line · Spotify · OS · Shell · Path · Git · Execution time · Copilot gauge |
| `wsezu.spotify` | Two-line · Spotify · OS · Shell · Path · Git · Execution time · Copilot gauge |
| `wsezu.og` | One-line · OS · Shell · Path · Git · Execution time · Copilot gauge |
| `wsezu.githubpremium` | One-line · OS · Shell · Path · Git · Copilot gauge only |
| `wsezu.simple` | One-line · minimal · OS · Copilot · Shell · Git |
| `wsezu.clean` | One-line · stripped back · OS · Shell · Git |

> Requires a [Nerd Font](https://www.nerdfonts.com/) for icons and powerline symbols.

---

## IaC

> 📁 `IaC/`

Infrastructure-as-code templates for cloud provisioning. Currently contains placeholder folders for:

- **`Bicep/`** — Azure Bicep ARM templates
- **`Terraform/`** — Terraform configurations

---

## Scripting

> 📁 `Scripting/`

Utility scripts for automation and productivity. Currently contains placeholder folders for:

- **`PowerShell/`** — Windows/cross-platform PowerShell scripts
- **`Python/`** — Python utility scripts

---

## License

This repository is licensed under the [GNU General Public License v3.0](./LICENSE).
