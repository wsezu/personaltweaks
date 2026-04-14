# Oh My Posh — Personal Themes

Personal collection of [Oh My Posh](https://ohmyposh.dev/) prompt themes. All themes are stored in the `Themes/` folder as `.omp.json` files and target **Oh My Posh v4** (schema v4).

## Themes Overview

| Theme file | Style | Segments |
|------------|-------|----------|
| `wsezu.full.omp.json` | Powerline · 2-line | Spotify · OS · Shell · Root · Path · Git — *(right)* Execution time · Copilot |
| `wsezu.spotify.omp.json` | Powerline · 2-line | Spotify · OS · Shell · Root · Path · Git — *(right)* Execution time · Copilot |
| `wsezu.og.omp.json` | Powerline · 1-line | OS · Shell · Root · Path · Git — *(right)* Execution time · Copilot |
| `wsezu.githubpremium.omp.json` | Powerline · 1-line | OS · Shell · Root · Path · Git — *(right)* Copilot |
| `wsezu.simple.omp.json` | Powerline · 1-line | OS · Copilot · Shell · Root · Git |
| `wsezu.clean.omp.json` | Powerline · 1-line | OS · Shell · Root · Git |

---

## Usage

Apply a theme in the current session:

```powershell
oh-my-posh init pwsh --config "path\to\Themes\wsezu.full.omp.json" | Invoke-Expression
```

To make it permanent, add the above line to your PowerShell profile (`$PROFILE`), replacing the config path with the full path to your chosen theme file.

> **Note:** A [Nerd Font](https://www.nerdfonts.com/) is required for all icons and powerline symbols to render correctly.