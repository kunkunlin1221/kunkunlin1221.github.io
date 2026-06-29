# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A Jekyll-based personal academic homepage using the [Minimal Light](https://github.com/yaoyao-liu/minimal-light) remote theme, deployed automatically to GitHub Pages.

## Commands

```bash
bundle install               # Install Ruby gem dependencies
bundle exec jekyll serve     # Local dev server at http://localhost:4000
```

No build step is needed before deploying — GitHub Pages builds Jekyll automatically on push to `main`.

## Architecture

Content is split across three layers:

**Data** (`_data/`) — YAML files are the source of truth for structured content. Edit these to add/update publications and projects:

- `publications.yml` — research papers (title, authors, venue, links, image)
- `projects.yml` — GitHub projects (name, description, image, links)

**Content** (`index.md` + `_includes/`) — The homepage is `index.md`, which uses `{% include %}` tags to pull in `publications.md`, `projects.md`, and `services.md`. Prose sections (About Me, Research Interests, News) are written directly in `index.md`.

**Layout/Styles** (`_layouts/homepage.html`, `_sass/`) — The single layout wraps all content. SCSS lives in `_sass/minimal-light.scss`; dark-mode-free variants (`*-no-dark-mode`) exist for both SCSS and CSS.

**Site config** (`_config.yml`) — Controls the remote theme, site metadata (name, position, affiliation), social links, dark mode toggle, font choice, and Google Analytics.

## Key conventions

- Images for publications and projects go in `assets/img/`; PDFs and slides go in `assets/files/`
- The `html_source_file/` directory contains pre-compiled HTML alternatives; it is excluded from the Jekyll build
- Dark mode is enabled via `auto_dark_mode: true` in `_config.yml`; the favicon switcher (`assets/js/favicon-switcher.js`) handles toggling between `favicon.jpg` and `favicon-dark.jpg`
