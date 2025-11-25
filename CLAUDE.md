# CLAUDE.md - AI Assistant Guide for raveenb.github.io

## Repository Overview

This is **Raveen's Personal Blog** - a GitHub Pages repository that hosts a personal website/blog at `https://raveenb.github.io`. The repository is currently in an early migration phase, with content being moved from a previous location.

## Current State

- **Status**: Early migration phase
- **Content**: Minimal - only README.md exists currently
- **Type**: GitHub Pages static site

## Repository Structure

### Expected GitHub Pages Structure

GitHub Pages repositories typically follow this structure:

```
/
├── _config.yml          # Jekyll configuration
├── _posts/              # Blog posts (YYYY-MM-DD-title.md format)
├── _layouts/            # HTML templates
├── _includes/           # Reusable HTML snippets
├── _sass/               # SCSS stylesheets
├── assets/              # Static assets (images, CSS, JS)
│   ├── css/
│   ├── js/
│   └── images/
├── _data/               # Data files (YAML, JSON, CSV)
├── _pages/              # Static pages
├── index.html           # Homepage
├── README.md            # Repository documentation
└── CLAUDE.md            # This file
```

### Current Files

- `README.md` - Repository description and migration notice

## Development Workflows

### Local Development

For Jekyll-based GitHub Pages sites:

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve --livereload

# Build the site
bundle exec jekyll build
```

### Creating Blog Posts

Blog posts should be created in the `_posts/` directory with the format:
- Filename: `YYYY-MM-DD-post-title.md`
- Front matter required at the top of each post

Example post front matter:
```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [category1, category2]
tags: [tag1, tag2]
---
```

### Deployment

- GitHub Pages automatically builds and deploys from the main branch
- No manual deployment steps required
- Changes pushed to main are live within minutes

## Key Conventions

### Naming Conventions

- **Posts**: Use kebab-case for post filenames: `YYYY-MM-DD-my-post-title.md`
- **Pages**: Use lowercase with hyphens: `about.md`, `contact.md`
- **Assets**: Organize by type in subdirectories

### Content Guidelines

- Use Markdown for all content
- Keep images optimized for web
- Use relative URLs for internal links
- Include alt text for all images

### Git Conventions

- **Commit messages**: Use clear, descriptive messages
- **Branch naming**: `feature/description` or `fix/description`
- **Main branch**: Production-ready content only

## AI Assistant Guidelines

### When Working on This Repository

1. **Respect the migration status** - Content is being migrated, so be prepared for incomplete structures

2. **Follow Jekyll conventions** - If adding content or templates, use standard Jekyll patterns

3. **Preserve existing content** - Do not remove or significantly modify existing posts without explicit instruction

4. **Test locally first** - Recommend testing Jekyll builds locally before pushing

5. **Optimize assets** - When adding images, ensure they are web-optimized

### Common Tasks

- **Adding a new post**: Create file in `_posts/` with proper naming and front matter
- **Updating styles**: Modify files in `_sass/` or `assets/css/`
- **Adding pages**: Create markdown files in root or `_pages/` directory
- **Configuration changes**: Edit `_config.yml` carefully, as it affects the entire site

### Things to Avoid

- Breaking Jekyll build with invalid YAML/Liquid syntax
- Adding very large unoptimized images
- Modifying `_config.yml` without understanding implications
- Creating posts with incorrect date format in filename

## Useful Commands

```bash
# Check Jekyll build for errors
bundle exec jekyll build --verbose

# Serve with drafts visible
bundle exec jekyll serve --drafts

# Clean build artifacts
bundle exec jekyll clean
```

## External Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
