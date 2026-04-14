# Theme Details

## `wsezu.full` & `wsezu.spotify`
The most feature-rich themes. Both are two-line layouts:
- **Line 1:** Spotify now-playing (artist – track, with play/pause/stop icons)
- **Line 2:** OS icon → Shell name → Root indicator → Current path (max 2 levels deep, agnoster-short style) → Git status
- **Right prompt:** Execution time (always shown) · GitHub Copilot premium usage gauge (cached 5 min)

## `wsezu.og`
One-line layout with a right prompt, similar to `wsezu.full` but without Spotify:
- **Left prompt:** OS icon → Shell name → Root indicator → Path → Git status
- **Right prompt:** Execution time · Copilot usage gauge

## `wsezu.githubpremium`
A focused variant that surfaces Copilot usage only (no execution time in right prompt):
- **Left prompt:** OS icon → Shell name → Root indicator → Path → Git status
- **Right prompt:** Copilot premium usage gauge

## `wsezu.simple`
Single-line, no path display — ideal for minimal or narrow terminals:
- OS icon → Copilot gauge → Shell name → Root indicator → Git status

## `wsezu.clean`
The most stripped-back custom theme — no Copilot widget, no path:
- OS icon → Shell name → Root indicator → Git status

---

# Shared Features

All `wsezu.*` themes share:

- **Git status** with colour-coded background:
  - 🟢 Green — clean
  - 🟠 Orange — working tree or staging changes
  - 🔵 Cyan — ahead of remote
  - 🔴 Red — diverged (ahead & behind)
- **Root/admin indicator** — dark red segment when running as root/admin
- **Console title** — `⚡ username ➔ 📁 foldername` (⚡ prefix when root)
- **Cross-platform OS icons** — Windows / macOS / Linux

---

# Usage

Apply a theme in the current session:

```powershell
oh-my-posh init pwsh --config "path\to\Themes\wsezu.full.omp.json" | Invoke-Expression
```

To make it permanent, add the above line to your PowerShell profile (`$PROFILE`), replacing the config path with the full path to your chosen theme file.

> **Note:** A [Nerd Font](https://www.nerdfonts.com/) is required for all icons and powerline symbols to render correctly.