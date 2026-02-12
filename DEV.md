# Development Guide

## Tech Stack

- **Hugo** - Static site generator
- **hugo-book** - Clean, documentation-style theme
- **Markdown** - Content format
- **SCSS** - Custom styling

## Development

### Prerequisites

- Hugo Extended (v0.155.0 or later)
- Go (for Hugo modules)

### Local Development

```bash
# Start the development server
hugo server -D

# Build for production
hugo --minify
```

The site will be available at `http://localhost:1313`

## Project Structure

```
imrajdas/
├── content/           # Markdown content
│   ├── _index.md     # Homepage
│   └── docs/         # Main content sections
│       ├── about.md
│       ├── now.md
│       ├── projects/
│       ├── blog/
│       └── uses.md
├── assets/           # Custom styles
├── .github/          # GitHub Actions workflows
├── hugo.yaml         # Hugo configuration
└── go.mod           # Hugo modules
```

## Deployment

This site can be deployed to:
- Netlify
- Vercel
- GitHub Pages
- Any static hosting service

See [GITHUB_PAGES_SETUP.md](GITHUB_PAGES_SETUP.md) for detailed deployment instructions.

## License

Content: © Raj Das
Code: MIT License

## Inspiration

Inspired by [geekodour.org](https://geekodour.org) and the digital garden movement.
