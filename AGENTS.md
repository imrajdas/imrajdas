# AI Agents Guide

This document provides context for AI coding assistants working on this project.

## Project Overview

**Portfolio Website for Raj Das**
- **Live Site**: https://rajdas.in
- **Tech Stack**: Hugo static site generator with hugo-book theme
- **Hosting**: GitHub Pages with custom domain
- **Repository**: https://github.com/imrajdas/imrajdas

## Project Structure

```
imrajdas/
├── content/              # Markdown content files
│   ├── _index.md        # Homepage content
│   ├── menu/            # Navigation menu configuration
│   └── docs/            # Main content sections
│       ├── about.md     # About page
│       ├── now.md       # Current activities
│       ├── projects/    # Projects showcase
│       ├── blog/        # Blog posts
│       └── uses.md      # Tools and setup
├── assets/              # Custom SCSS styles
│   └── _custom.scss     # Theme customizations
├── .github/workflows/   # CI/CD automation
│   └── main.yml         # GitHub Actions deployment workflow
├── hugo.yaml            # Hugo configuration
├── go.mod               # Hugo modules (theme management)
├── netlify.toml         # Netlify deployment config (alternative)
└── public/              # Generated static site (gitignored)
```

## Key Configuration Files

### hugo.yaml
- **baseURL**: Must be `https://rajdas.in/` for correct asset paths
- **Theme**: hugo-book (loaded via Go modules)
- **Features**: Search enabled, ToC enabled, comments disabled

### .github/workflows/main.yml
- **Trigger**: Pushes to `main` branch
- **Build**: Hugo 0.155.3 extended with Go 1.21
- **Deploy**: GitHub Pages via Actions
- **Important**: baseURL must match custom domain for CSS to load

## Content Management

### Adding Content
- All content is in Markdown format
- Front matter uses YAML
- Files in `content/docs/` appear in sidebar navigation
- Use `weight` parameter to control ordering

### Navigation
- Configured in `content/menu/index.md`
- Uses Hugo's relref for internal links
- Automatically generated from content structure

## Deployment

### Automatic Deployment
- Push to `main` branch triggers GitHub Actions
- Build takes ~1-2 minutes
- Site updates automatically at https://rajdas.in

### Manual Testing
```bash
# Local development server
hugo server -D

# Production build
hugo --minify
```

## Common Tasks

### Update About Page
Edit `content/docs/about.md` with professional bio and links.

### Add Blog Post
Create new file in `content/docs/blog/` with front matter:
```yaml
---
title: "Post Title"
date: 2026-02-13
weight: 1
---
```

### Add Project
Create new file in `content/docs/projects/` or edit `_index.md`.

### Customize Styling
Edit `assets/_custom.scss` for theme overrides.

## Important Notes

### baseURL Configuration
- **Critical**: baseURL in `hugo.yaml` and `.github/workflows/main.yml` must match
- Must be `https://rajdas.in/` (not subdirectory path)
- Incorrect baseURL causes CSS/JS to fail loading

### DNS Configuration
- Domain: rajdas.in (GoDaddy)
- A records point to GitHub Pages IPs
- CNAME for www subdomain
- See `GITHUB_PAGES_SETUP.md` for details

### Theme Customization
- Theme loaded via Hugo modules (not git submodule)
- Custom styles in `assets/_custom.scss`
- Override layouts by creating files in `layouts/` directory

## Troubleshooting

### CSS Not Loading
- Check baseURL in both `hugo.yaml` and workflow file
- Ensure custom domain is configured in GitHub Pages settings
- Verify DNS records are correct

### Build Failures
- Check Hugo version compatibility (0.155.3 extended)
- Ensure Go modules are up to date: `hugo mod get -u`
- Review GitHub Actions logs for specific errors

### Content Not Appearing
- Verify front matter is valid YAML
- Check `draft: false` (or use `-D` flag locally)
- Ensure file is in correct directory structure

## Development Workflow

1. **Local Changes**
   ```bash
   hugo server -D
   # Test at http://localhost:1313
   ```

2. **Commit & Push**
   ```bash
   git add .
   git commit -m "Description"
   git push
   ```

3. **Automatic Deployment**
   - GitHub Actions builds and deploys
   - Check Actions tab for status
   - Site updates in 1-2 minutes

## Resources

- **Hugo Documentation**: https://gohugo.io/documentation/
- **hugo-book Theme**: https://github.com/alex-shpak/hugo-book
- **GitHub Pages**: https://docs.github.com/en/pages
- **Development Guide**: See `DEV.md`
- **Deployment Guide**: See `GITHUB_PAGES_SETUP.md`

## Contact

- **Owner**: Raj Das
- **GitHub**: @imrajdas
- **Site**: https://rajdas.in

---

*Last updated: February 2026*
