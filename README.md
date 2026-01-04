# Matt Anderson's Personal Website

Personal portfolio and blog built with Hugo and the PaperMod theme.

🌐 **Live Site:** [mattanderson.xyz](https://mattanderson.xyz)

## Tech Stack

- **Static Site Generator:** [Hugo](https://gohugo.io/) v0.153.4+
- **Theme:** [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **Hosting:** GitHub Pages / Custom Domain

## Quick Start

### Prerequisites

- Hugo Extended v0.146.0 or higher
- Git

### Development

```bash
# Start local development server
hugo server -D

# Server will be available at http://localhost:1313
```

### Build

```bash
# Build production site (outputs to public/)
hugo

# Build with drafts included
hugo -D
```

## Project Structure

```
.
├── content/          # Markdown content files
│   ├── _index.md    # Home page bio section
│   └── contact.md   # Contact page
├── layouts/         # Custom layout overrides
│   └── _default/
│       └── list.html # Custom home page layout
├── static/          # Static assets (served directly)
│   ├── profile.jpg  # Profile image
│   └── resume.pdf   # Resume PDF
├── assets/          # Assets processed by Hugo
│   └── css/
│       └── extended/
│           └── custom.css # Custom CSS overrides
├── themes/          # Hugo themes (git submodule)
│   └── papermod/    # PaperMod theme
└── hugo.toml        # Site configuration
```

## Content Management

### Creating New Content

```bash
# Create a new blog post
hugo new posts/my-post-name.md

# Create other content
hugo new <section>/<filename>.md
```

### Front Matter

Content files use TOML front matter:

```toml
+++
title = 'Page Title'
date = 2026-01-04T00:00:00Z
draft = false
+++
```

## Theme Management

The PaperMod theme is managed as a git submodule.

```bash
# Update theme to latest version
git submodule update --remote --merge

# Initialize submodules (after fresh clone)
git submodule update --init --recursive
```

### Customization

- **Configuration:** Edit `hugo.toml` for site settings
- **Layout Overrides:** Add files to `layouts/` directory
- **Custom CSS:** Add styles to `assets/css/extended/custom.css`

**Important:** Do not modify files in `themes/papermod/` directly.

## Site Configuration

Key configuration in `hugo.toml`:

- Profile mode enabled with custom title and subtitle
- Social icons (GitHub, LinkedIn, Resume)
- Contact page in main menu
- Unsafe HTML rendering enabled for custom forms

## Deployment

The site is deployed via GitHub Pages. Push to the `main` branch to trigger deployment.

```bash
# Commit changes
git add .
git commit -m "Your commit message"

# Push to GitHub
git push origin main
```

## Contact

- **Email:** me@mattanderson.xyz
- **LinkedIn:** [matt-anderson-dev](https://www.linkedin.com/in/matt-anderson-dev/)
- **GitHub:** [sgmaniakk](https://github.com/sgmaniakk)

## License

Personal website - All rights reserved.
