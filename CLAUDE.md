# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal academic website for Duncan Watson-Parris (atmospheric physicist) built with Jekyll and hosted on GitHub Pages. It uses the [jekyll-theme-prologue](https://github.com/chrisbobbe/jekyll-theme-prologue) remote theme.

## Development Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload (access at http://localhost:4000)
bundle exec jekyll serve

# Build the site (outputs to _site/)
bundle exec jekyll build
```

Note: After changing `_config.yml`, you must restart the server.

## Site Structure

- **`_sections/`** - Homepage content sections (rendered in order by `order` frontmatter)
- **`_layouts/`** - Page templates (home, page, post, blog, default)
- **`_includes/`** - Reusable HTML partials (nav, header, footer, social_icons)
- **`_posts/`** - Blog posts (standard Jekyll format: `YYYY-MM-DD-title.md`)
- **`assets/`** - Static files (images, CSS, JS)
- **`_site/`** - Generated output (do not edit directly)

## Key Configuration

The `_config.yml` contains:
- Site metadata (title, description, author, email)
- Social profile URLs (Bluesky, LinkedIn, GitHub, Google Scholar)
- Google Analytics tracking ID
- Collections: `sections`, `projects`, `pub_types`

## Adding Content

### New homepage section
Create a file in `_sections/` with frontmatter:
```yaml
---
title: Section Title
order: 3
icon: fa-icon-name
---
```

### New page
Create `.html` or `.md` file in root with:
```yaml
---
title: Page Title
layout: page
order: 2
---
```
