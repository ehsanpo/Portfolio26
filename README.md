# Portfolio26

A modern, multi-language portfolio website built with Next.js, TypeScript, and a custom design system.

## Project Structure

```
├── ui kit/           # Component library
│   ├── atoms/        # Basic UI elements (buttons, inputs, etc.)
│   ├── components/   # Composite components (navbar, cards, etc.)
│   └── blocks/       # Page-level sections (hero, project grid, etc.)
├── design system/    # Design tokens and guidelines
├── website/          # Next.js application
├── content/          # Markdown content with co-located images
│   ├── portfolio/    # Portfolio projects and case studies
│   └── blog/         # Blog posts
├── data/             # Global JSON data
│   ├── portfolio.json # Site-wide configuration and copy
│   └── resume.json   # Resume/CV data
└── docs/             # Documentation and planning
```

## Features

- 🌍 **Multi-language support** (English, Swedish, Persian with RTL)
- 🎨 **Custom design system** with CSS variables
- 📱 **Fully responsive** and accessible
- 🚀 **Performance optimized** with Next.js App Router
- 📝 **Markdown-based content** with co-located images
- 🔄 **Automatic translation** pipeline for missing locales
- 📊 **Analytics ready** with Vercel Analytics

## Tech Stack

- **Framework:** Next.js 14+ (App Router) with TypeScript
- **Styling:** CSS Modules + CSS Variables (custom design system)
- **Icons:** Lucide React
- **Content:** Markdown with frontmatter
- **Internationalization:** Next.js i18n with auto-translation
- **Analytics:** Vercel Analytics

## Getting Started

This project is currently in development. Follow the implementation phases:

### Phase 0: ✅ Repository Structure
- [x] Create folder structure
- [x] Set up basic configuration files
- [x] Initialize data files

### Phase 1: 🚧 Design System
- [ ] Define design tokens (colors, typography, spacing)
- [ ] Create CSS variable system
- [ ] Set up light/dark themes
- [ ] Add RTL support

### Phase 2: 🔄 UI Kit
- [ ] Build atomic components (buttons, inputs, etc.)
- [ ] Create composite components (navbar, cards, etc.)  
- [ ] Develop page blocks (hero, project grid, etc.)

### Phase 3: 🔄 Website Implementation
- [ ] Set up Next.js application
- [ ] Implement routing and i18n
- [ ] Create block registry system
- [ ] Build content pipeline

### Phase 4: 🔄 Content & Polish
- [ ] Add real content and images
- [ ] Optimize performance
- [ ] Implement SEO
- [ ] Add accessibility features

### Phase 5: 🔄 Deployment
- [ ] Deploy to Vercel
- [ ] Set up monitoring
- [ ] Configure CI/CD

## Development Workflow

Each phase is developed in separate branches with pull requests for review:

- `phase-0/*` - Repository setup and configuration
- `phase-1/*` - Design system implementation  
- `phase-2/*` - UI Kit development
- `phase-3/*` - Website application
- `phase-4/*` - Content and optimization
- `phase-5/*` - Deployment and monitoring

## Conventions

- **File naming:** kebab-case for files and folders
- **Components:** PascalCase for React components
- **Functions:** camelCase for TypeScript functions
- **Git:** Conventional Commits with descriptive PRs
- **Accessibility:** WCAG 2.1 AA compliance target

## License

MIT License - see LICENSE file for details