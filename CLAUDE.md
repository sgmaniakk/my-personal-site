# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website built with Hugo static site generator, using the PaperMod theme. The site is configured with minimal customization at this stage.

## Core Commands

### Development
```bash
# Start local development server with drafts enabled
hugo server -D

# Start server on custom port
hugo server -D -p 1313

# Build the site (outputs to public/)
hugo

# Build with drafts included
hugo -D
```

### Content Management
```bash
# Create a new post (will be placed in content/)
hugo new posts/my-post-name.md

# Create new content using default archetype
hugo new <section>/<filename>.md
```

### Theme Management
```bash
# Update the PaperMod theme submodule
git submodule update --remote --merge

# Initialize submodules (needed after fresh clone)
git submodule update --init --recursive
```

## Architecture

### Site Structure
- `hugo.toml` - Main configuration file for site settings, theme selection, and parameters
- `content/` - Markdown files for all site content (posts, pages)
- `static/` - Static assets (images, files) served directly
- `layouts/` - Custom layout overrides for the theme
- `archetypes/` - Templates for new content (defines front matter structure)
- `themes/papermod/` - Git submodule containing the PaperMod theme
- `public/` - Generated static site output (not committed to git)

### Theme System
The site uses Hugo PaperMod theme as a git submodule. Do not modify files directly in `themes/papermod/`. Instead:
- Override layouts by creating corresponding files in the root `layouts/` directory
- Customize configuration through `hugo.toml`
- Add custom CSS/JS through `assets/` directory

### Content Architecture
- Posts use front matter (TOML format by default) with `date`, `draft`, and `title` fields
- The `draft = true` flag prevents content from appearing in production builds
- Content files are organized by section (directory name becomes the section)

## Important Notes

- Hugo version requirement: >= v0.146.0 (currently using v0.153.4)
- The theme is managed as a git submodule - use git submodule commands to update
- Always run `hugo server -D` during development to preview draft content
- The `public/` directory is regenerated on each build and should not be edited manually
