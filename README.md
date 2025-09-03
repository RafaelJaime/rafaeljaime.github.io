# Rafael Jaime's Portfolio

Personal portfolio built with [Hugo](https://gohugo.io/) and automatically deployed to GitHub Pages.

## Multilingual Site

Available in two languages with English as the default:
- **English** (default): `https://rafaeljaime.github.io/en/`
- **Spanish**: `https://rafaeljaime.github.io/es/`

Accessing `https://rafaeljaime.github.io/` automatically redirects to `/en/`.

## Technologies

- **Hugo** - Static site generator
- **PaperMod** - Hugo theme
- **GitHub Actions** - Automated CI/CD
- **GitHub Pages** - Hosting

## Project Structure

```
├── content/
│   ├── about.md              # About page (English)
│   ├── about.es.md           # About page (Spanish)
│   └── projects/
│       ├── _index.md         # Projects list (English)
│       ├── _index.es.md      # Projects list (Spanish)
│       ├── example-project.md
│       └── proyecto-ejemplo.es.md
├── layouts/                  # Custom layouts
├── static/
│   └── index.html           # Auto-redirect page
├── themes/PaperMod/         # Theme (git submodule)
├── hugo.toml                # Main configuration
└── .github/workflows/       # GitHub Actions
```

## Local Development

### Prerequisites
- [Hugo Extended](https://gohugo.io/installation/) v0.149.0+
- Git

### Setup
1. Clone the repository:
```bash
git clone --recursive https://github.com/RafaelJaime/rafaeljaime.github.io.git
cd rafaeljaime.github.io
```

2. Start development server:
```bash
hugo server --buildDrafts
```

3. Visit:
   - `http://localhost:1313` (redirects to `/en/`)
   - `http://localhost:1313/en/` (English)
   - `http://localhost:1313/es/` (Spanish)

## Adding Content

### New page
English: `hugo new content page-name.md`
Spanish: `hugo new content page-name.es.md`

### New project
English: `hugo new content projects/project-name.md`
Spanish: `hugo new content projects/nombre-proyecto.es.md`

## Deployment

Automatically deployed via GitHub Actions on push to `main` branch.
