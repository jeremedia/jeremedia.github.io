# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Jekyll-based personal blog hosted on GitHub Pages at https://jeremedia.github.io. The blog uses a minimalist design with Berkeley Mono font and focuses on technology and literacy topics.

## Development Commands

```bash
# Install dependencies
bundle install

# Run local development server (http://localhost:4000)
bundle exec jekyll serve

# Build site (for testing production build locally)
JEKYLL_ENV=production bundle exec jekyll build
```

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the main branch:

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

No manual build or deployment steps are required - GitHub Pages handles the Jekyll build automatically.

## Project Structure

- **_posts/**: Blog posts in Markdown format with YAML front matter
- **_layouts/**: Custom HTML templates (default.html, post.html)
- **assets/**: Static assets including CSS, fonts, and images
- **_config.yml**: Jekyll configuration and site metadata
- **index.html**: Homepage with hero image and post listings
- **about.md**: About page with professional background

## Creating New Posts

Create files in `_posts/` with the naming convention `YYYY-MM-DD-title-slug.md`:

```markdown
---
layout: post
title: "Post Title"
date: YYYY-MM-DD
categories: category-name
---

Post content here...
```

## Key Configuration

The site uses the `github-pages` gem to ensure compatibility with GitHub's Jekyll environment. All plugins and dependencies are managed through this gem to match GitHub's build environment exactly.

## Style Guidelines

- The site uses Berkeley Mono font throughout
- Minimalist design with focus on readability
- Hero image on homepage displays at 100% width
- No JavaScript frameworks or build tools - pure Jekyll/HTML/CSS