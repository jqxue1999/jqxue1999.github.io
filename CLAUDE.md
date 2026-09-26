# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static academic homepage for Jiaqi Xue (jqxue1999.github.io), a Ph.D. student at UCF. Deployed via GitHub Pages directly from the `master` branch — no build step, no frameworks, no package manager.

## Deployment

Push to `master` triggers GitHub Pages deployment automatically. No build commands needed.

## Architecture

- `index.html` — the entire site is a single HTML file using jemdoc CSS styling
- `files/` — static assets: CSS (`jemdoc.css`), images, paper PDFs, analytics script (`ga.js`)
- `cv/resume.tex` — LaTeX source of the CV; compile in place to `cv/resume.pdf`, which the homepage links to. Build artifacts are git-ignored. Keep the CV's Biography and publication list in sync with `index.html`.

## Publication Entry Format

Publications have no tag badges. Each `<li>` entry follows this pattern:
```html
<li>
    <a href='PAPER_URL'>Paper Title</a><br>
    Author1, <strong><u>Jiaqi Xue</u></strong>, Author2<br>
    Conference Name <strong>(ABBREV)</strong>, Year <br>
</li>
```

The author's own name is always bolded and underlined: `<strong><u>Jiaqi Xue</u></strong>`. Equal contribution is marked with `*`. Publications are listed in reverse chronological order.