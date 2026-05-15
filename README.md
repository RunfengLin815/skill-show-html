# skill-show-html

A Claude Code skill that generates interactive HTML review pages with per-section commenting.

## What it does

When Claude produces structured content that needs user review (architecture decisions, technical proposals, design reviews, research reports, etc.), this skill renders it as a self-contained HTML page with built-in commenting capabilities.

## Key Features

- **Per-section comments** — Every section has a collapsible comment box with full CRUD (create, edit, delete)
- **Attitude markers** — Quick approve / question / reject buttons per section
- **Review progress** — Shows how many sections have been reviewed
- **Export** — One-click export of all comments to clipboard, ready to paste back into Claude Code
- **Self-contained** — No external dependencies, works offline
- **Print-friendly** — `@media print` hides interactive elements

## Install

```bash
# Claude Code CLI
claude skill add /path/to/skill-show-html
```

Or copy `SKILL.md` to `~/.claude/skills/show-html/SKILL.md`.

## Usage

The skill triggers automatically when Claude generates reviewable content. You can also invoke it explicitly:

```
/show-html <topic>
```

## Workflow

1. Claude generates an HTML page and opens it in your browser
2. Review each section — mark attitude, write comments
3. Click "Export all comments" — copied to clipboard
4. Paste back into Claude Code to continue the discussion
