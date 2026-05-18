# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an **Obsidian vault** used as a personal knowledge management system, synced between devices using Google Drive + DriveSync (Android). The vault contains philosophy notes, college coursework, creative writing, project documentation, and daily notes.

## Directory Structure

| Directory | Purpose |
|-----------|---------|
| `philosophy/` | Personal philosophy notes and reflections (organized with waypoints) |
| `notes/` | Academic notes organized by semester and course (S2, S3, etc.) |
| `projects/` | Personal project documentation (code snippets, tools, ideas) |
| `planning/` | Schedules, weekly plans, reflections |
| `obsidian/` | Obsidian configuration, templates, daily notes |
| `movi/` | Creative writing (fiction/worldbuilding) |
| `games/` | Gaming notes (Elden Ring builds, Minecraft) |
| `thoughts/` | Miscellaneous thoughts and ideas |
| `resources/` | External resource links |
| `images/` | Image attachments |

## Key Obsidian Configuration

**Core Settings** (`.obsidian/app.json`):
- New notes created in `obsidian/new_notes`
- Attachments stored in `images/` folder
- Vim mode enabled, line numbers shown
- Auto-update links enabled

**Community Plugins** (`.obsidian/community-plugins.json`):
- Navigation: `homepage`, `waypoint`, `calendar`, `better-search-views`
- Organization: `obsidian-kanban`, `obsidian-timeline`, `obsidian-icon-folder`
- Writing: `callout-manager`, `text-snippets-obsidian`, `obsidian-underline`
- Visual: `obsidian-excalidraw-plugin`, `obsidian-minimal-settings`

**Daily Notes** (`.obsidian/daily-notes.json`):
- Location: `obsidian/dailynotes/`
- Format: `DDMMYY-ddd` (e.g., `190425-Fri`)
- Template: `obsidian/templates/dailynote_template`

## Conventions

### Waypoints
Directory index files use Waypoint comments to auto-generate file trees:
```markdown
%% Begin Waypoint %%
- [[note1]]
- [[note2]]
%% End Waypoint %%
```

### File Naming
- Daily notes: `DDMMYY-ddd.md` format
- Philosophy notes: snake_case
- Course notes: organized by semester (`S2/`, `S3/`) and course codes (`_LSPC_`, `_EEIPR_`, `_CP_`)

### Sync Setup
Vault syncs via Google Drive (desktop) + DriveSync app (Android) with ~5 minute sync intervals. See `obsidian/sync/drivesync_method.md` for setup details.
