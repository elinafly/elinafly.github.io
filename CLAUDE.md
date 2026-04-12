# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static academic personal website. No build tooling or dependencies — pure HTML + CSS.

## Structure

```
index.html      — About / home page
research.html   — Working papers, publications, work in progress
teaching.html   — Current and past courses
cv.html         — Full CV with PDF download button
contact.html    — Email, office, social/academic profiles
css/style.css   — All styles (single shared stylesheet)
files/cv.pdf    — CV PDF to upload (not yet present)
```

## Running Locally

Open any `.html` file directly in a browser. If you need a local server (e.g. to test PDF links):

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Design System

All design tokens are CSS custom properties at the top of `css/style.css` (`:root`). Key tokens:
- `--lavender` / `--lavender-dark` / `--lavender-pale` — primary accent palette
- `--bg-card` — card backgrounds
- `--radius-pill` — oval/pill button border-radius (50px)
- `--max-w` — page content max-width (780px)

Shared components in the stylesheet: `.btn-primary`, `.btn-outline`, `.card`, `.tag`, `.cv-entry`, `.course-row`, `.contact-item`.

## Adding Content

- Replace all `[placeholder]` text in HTML files with real content.
- To add a profile photo: place image in `images/` and replace the `.about-avatar-placeholder` div in `index.html` with `<img src="images/photo.jpg" ... class="about-avatar" />`.
- To enable CV download: place `cv.pdf` in a `files/` folder. The download button in `cv.html` already points to `files/cv.pdf`.
- Navigation `class="active"` is set per-page manually on the matching `<a>` tag.

## Remote

GitHub repository: `https://github.com/elinafly/my-website`
