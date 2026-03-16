# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static academic homepage for Jiaqi Xue (jqxue1999.github.io), a Ph.D. student at UCF. Deployed via GitHub Pages directly from the `master` branch — no build step, no frameworks, no package manager.

## Deployment

Push to `master` triggers GitHub Pages deployment automatically. No build commands needed.

## Architecture

- `index.html` — the entire site is a single HTML file using jemdoc CSS styling
- `files/` — static assets: CSS (`jemdoc.css`), images, CV PDF, analytics script (`ga.js`)

## Publication Entry Format

Publications use colored tag badges followed by paper details. Tag colors:
- **Efficiency**: `#28a745` (green)
- **Privacy**: `#007bff` (blue)
- **Safety**: `#dc3545` (red)
- **Agent**: `#6f42c1` (purple)

Each `<li>` entry follows this pattern:
```html
<li>
    <span style="background-color:#COLOR;color:white;padding:2px 8px;border-radius:3px;font-size:12px;font-weight:bold;margin-right:6px;">TAG</span>
    <a href='PAPER_URL'>Paper Title</a><br>
    Author1, <strong><u>Jiaqi Xue</u></strong>, Author2<br>
    Conference Name <strong>(ABBREV)</strong>, City, Country, Year <br>
</li>
```

The author's own name is always bolded and underlined: `<strong><u>Jiaqi Xue</u></strong>`. Equal contribution is marked with `*`. Publications are listed in reverse chronological order.