# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an academic website built with the **al-folio** Jekyll theme. It's a personal academic portfolio site hosted on GitHub Pages that includes blog posts, publications, projects, and CV sections.

## Build and Development Commands

### Local Development (Docker - Recommended)
```bash
# Pull and run the site locally
docker compose pull
docker compose up

# Access at: http://localhost:8080
```

### Local Development (Legacy Ruby/Jekyll)
```bash
# Install dependencies
bundle install
pip install jupyter

# Serve locally
bundle exec jekyll serve
# Access at: http://localhost:4000
```

### Build for Production
```bash
# Set environment and build
export JEKYLL_ENV=production
bundle exec jekyll build

# Purge unused CSS (optional)
purgecss -c purgecss.config.js
```

### Code Formatting
```bash
# Format code with Prettier
npx prettier . --write

# Check formatting
npx prettier . --check
```

## Architecture

### Site Structure
- **Jekyll Static Site**: Uses Jekyll for static site generation
- **GitHub Pages Deployment**: Automatically deploys via GitHub Actions on push to main/master
- **Collections**: Organized into books, news, projects, and posts collections
- **Dynamic Content**: Supports Jupyter notebooks, publications from BibTeX, and academic features

### Key Directories
- `_posts/`: Blog posts in Markdown
- `_pages/`: Static pages (about, blog, CV, etc.)  
- `_projects/`: Project showcase entries
- `_layouts/`: Jekyll layout templates
- `_includes/`: Reusable template components
- `_sass/`: SCSS stylesheets
- `assets/`: Static assets (images, CSS, JS, PDFs)
- `_bibliography/`: BibTeX files for publications

### Content Types
- **Blog Posts**: Markdown files with YAML front matter in `_posts/`
- **Publications**: Managed via BibTeX files in `_bibliography/`
- **Projects**: Collection items in `_projects/` directory
- **CV**: Can use JSON resume format or YAML data files
- **Jupyter Notebooks**: Supported via jekyll-jupyter-notebook plugin

### Configuration
- Main config: `_config.yml` - contains site settings, plugins, and theme configuration
- Personal info configured in `_config.yml` (name, description, social links)
- Publication settings in scholar section of config
- Third-party library versions managed in config file

## Deployment

- **Automatic**: GitHub Actions automatically builds and deploys on push to main/master branch
- **Manual Trigger**: Can manually trigger deployment via GitHub Actions "Deploy" workflow
- **Target**: Deploys to `gh-pages` branch, served by GitHub Pages

## Development Notes

- Uses Ruby 3.3.5 and Python 3.13 in CI/CD
- Docker development environment available for consistent local setup
- Prettier formatting enforced via GitHub Actions
- Supports responsive images via imagemagick processing
- Academic features: bibliography management, math typesetting, syntax highlighting