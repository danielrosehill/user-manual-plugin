# User Manual Plugin

[![Claude Code Repos Index](https://img.shields.io/badge/Claude_Code-Repos_Index-blue?style=for-the-badge&logo=github)](https://github.com/danielrosehill/Claude-Code-Repos-Index)

![Claude Code](https://img.shields.io/badge/Claude_Code-Plugin-8A2BE2?style=for-the-badge&logo=anthropic)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

A Claude Code plugin for generating personal user manuals and private documentation for codebases. Creates personalized, private reference guides with PDF output support.

## Purpose

Most tech documentation prompts assume public-facing docs for open source projects. This plugin is designed for a different use case: **creating documentation for yourself**.

Use this plugin when you need:
- Notes-to-self for repositories or processes created by AI agents
- A personal reference guide for how something was set up
- Memory aids for future maintenance of automated systems
- Private documentation that may include credentials, specific configurations, or internal feature details

## Installation

```bash
/plugin install user-manual@danielrosehill
```

Or install from the marketplace:

```bash
/plugin marketplace add https://github.com/danielrosehill/Claude-Code-Plugins
/plugin install user-manual@danielrosehill
```

## Available Commands

| Command | Description |
|---------|-------------|
| `/user-manual:user-manual` | Generate a complete personal user manual (full workflow) |
| `/user-manual:doc-setup` | Set up documentation folder structure (Step 1 of 4) |
| `/user-manual:generate-parts` | Generate individual documentation sections (Step 2 of 4) |
| `/user-manual:create-pdf` | Compile sections into a formatted PDF (Step 3 of 4) |
| `/user-manual:disseminate` | Version control and distribute the manual (Step 4 of 4) |
| `/user-manual:create-private-repo` | Create a private GitHub repository for the project |

## Workflows

### Full Workflow (Recommended)

Run `/user-manual:user-manual` for a complete end-to-end documentation generation that handles everything automatically.

### Step-by-Step Workflow

For more control, run the commands sequentially:

1. **`/user-manual:doc-setup`** - Creates `docs/` folder with `sections/`, `assets/`, and `output/` subdirectories
2. **`/user-manual:generate-parts`** - Engages a documentation agent to generate markdown sections
3. **`/user-manual:create-pdf`** - Compiles sections into a formatted PDF (prefers Typst, falls back to Pandoc)
4. **`/user-manual:disseminate`** - Commits to git and optionally distributes via MCP

## Key Features

- **Private by default** - Documentation can include credentials, internal details, and feature outlines
- **Personalized tone** - Friendlier voice than public docs while maintaining technical accuracy
- **Versioned** - Tracks version numbers across iterations
- **Professional output** - PDF generation with IBM Plex Sans font, page numbers, and Mermaid diagrams
- **MCP integration** - Optional distribution to cloud storage, Notion, or email via Resend

## Output Format

The generated user manual includes:
- Title page with your name, project title, version, and date
- Section-by-section documentation with code samples in proper fences
- Mermaid diagrams where appropriate
- Page numbers in footer
- IBM Plex Sans typography

## Plugin Structure

```
user-manual-plugin/
├── .claude-plugin/
│   └── plugin.json           # Plugin manifest
├── commands/
│   ├── user-manual.md        # Full workflow command
│   ├── doc-setup.md          # Step 1: Setup
│   ├── generate-parts.md     # Step 2: Generate sections
│   ├── create-pdf.md         # Step 3: Compile PDF
│   ├── disseminate.md        # Step 4: Distribute
│   └── create-private-repo.md # Utility command
├── skills/
│   └── documentation-writer/
│       └── SKILL.md          # Documentation writing skill
├── README.md
└── LICENSE
```

## License

MIT

## Author

**Daniel Rosehill**
- Website: [danielrosehill.com](https://danielrosehill.com)
- Email: public@danielrosehill.com
- GitHub: [@danielrosehill](https://github.com/danielrosehill)

---

For more Claude Code projects, visit my [Claude Code Repos Index](https://github.com/danielrosehill/Claude-Code-Repos-Index).
