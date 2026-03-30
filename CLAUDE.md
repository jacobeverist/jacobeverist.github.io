# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal GitHub Pages site for Jacob Everist, built with Jekyll and deployed automatically via GitHub Actions on every push to `main`. The site uses the `dinky` remote theme.

## Local Development

```bash
bundle install          # Install dependencies
bundle exec jekyll serve  # Serve locally at http://localhost:4000
```

The `_site/` directory contains built output and is gitignored.

## Site Structure

The site uses the `academicpages/academicpages.github.io` remote theme.

- **`_pages/`** — All site content pages (about, publications, projects, cv). The `about.md` has `permalink: /` making it the home page.
- **`_data/navigation.yml`** — Top navigation links.
- **`_config.yml`** — Site config including `author:` block (name, bio, avatar, social links) that drives the sidebar on every page.
- **`README.md`** / **`CV.md`** — Legacy content; content has been migrated into `_pages/`.
- **`Gemfile`** — Uses `github-pages` and `jekyll-remote-theme` gems.

## Deployment

Pushing to `main` triggers `.github/workflows/jekyll-gh-pages.yml`, which builds with Jekyll and deploys to GitHub Pages automatically. No manual deployment steps needed.

## Content Editing

All content is Markdown. The site has no custom layouts, includes, or assets directories — the remote `dinky` theme provides all styling and templating.
