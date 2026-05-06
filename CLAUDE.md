# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal resume/portfolio website hosted on GitHub Pages at `https://sukainaalkhalidy.github.io`. No build step or package manager — all changes to `index.html`, `style.css`, or `script.js` are deployed by pushing to `origin main`.

## Deploying changes

```bash
git add index.html   # or style.css / script.js
git commit -m "your message"
git push origin main
```

GitHub Pages serves the updated site within ~1–2 minutes of a push.

## File structure

- `index.html` — single-page site; all content (About, Projects, Certifications, Resume) lives here. CSS is partly inline (`<style>` in `<head>`) and partly in `style.css`.
- `style.css` — external styles (supplements the inline block).
- `script.js` — currently empty.
- `resume.pdf` — linked with a cache-busting query string (currently `?v=6`); increment the version number whenever the PDF is replaced.
- `profile.jpg`, `myphoto.jpg` — profile photos.
- `CMSE492_FinalProject_Report.pdf`, `Taxi_Report_Basic.pdf` — project reports linked from the Projects section.

## Page sections (by anchor)

| Anchor | Section |
|---|---|
| `#about` | About Me |
| `#experience` | Projects |
| `#certs` | Certifications |
| `#resume-preview` | Resume (PDF embed + download) |

## Key content locations in index.html

- Contact info & education: `<header>` (~line 139)
- Projects list: `<section id="experience">` (~line 160)
- Certifications list: `<section id="certs">` (~line 193)
- Resume embed: `<section id="resume-preview">` (~line 202)
