# Marginalia — Obsidian Plugin

Scan your vault for quality issues, discover missing links between notes, and auto-fix frontmatter.

Powered by the [marginalia CLI](https://github.com/hale-bopp-data/marginalia) (`pip install marginalia`).

## Features

- **Scan** — Find broken links, missing frontmatter, orphan notes, tag issues, and more
- **Link suggestions** — Discover related notes that should be linked together
- **Auto-fix** — Fix frontmatter, normalize tags, and apply link suggestions in bulk
- **Side panel** — All results displayed in a dedicated Obsidian panel
- **Commands** — All actions available via `Ctrl/Cmd+P`

## Installation

### 1. Install the marginalia CLI

```bash
pip install marginalia
```

### 2. Install the Obsidian plugin

**From Community Plugins (recommended):**

1. Open Obsidian Settings > Community Plugins
2. Search for "marginalia"
3. Install and enable

**Manual install:**

1. Download `main.js`, `manifest.json`, and `styles.css` from the [latest release](https://github.com/hale-bopp-data/obsidian-marginalia/releases)
2. Create a folder `<your-vault>/.obsidian/plugins/marginalia/`
3. Copy the three files into that folder
4. Restart Obsidian and enable the plugin in Settings > Community Plugins

## First launch

On first launch, the plugin auto-detects your Python/marginalia installation.
If found, you're ready to go. If not, it guides you through setup.

## Commands

| Command | Description |
|---------|-------------|
| `marginalia: Scan vault for issues` | Full vault quality scan |
| `marginalia: Suggest related links` | Discover missing links |
| `marginalia: Apply link suggestions (dry-run)` | Preview what would change |
| `marginalia: Apply link suggestions (WRITE)` | Actually write the links |
| `marginalia: Fix pipeline (dry-run)` | Preview auto-fixes |
| `marginalia: Fix pipeline (apply)` | Apply auto-fixes |
| `marginalia: Check CLI installation` | Verify marginalia is installed |

## Settings

- **Executable path** — Point to your `marginalia` binary or use `python -m marginalia`
- **Minimum score** — Filter link suggestions by relevance (0–1)
- **Max links per file** — Cap on "See Also" links added
- **Scope** — Apply to all files or orphans only

## Requirements

- Obsidian 1.4.0+
- Python 3.9+
- marginalia CLI (`pip install marginalia`)

## License

MIT
