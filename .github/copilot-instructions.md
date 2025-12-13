# Copilot Instructions for brittanychiang.com Portfolio

## Overview

This is a Gatsby-based personal portfolio website. Content is authored in Markdown and processed into static pages. The site features a single-page application layout with smooth scrolling sections.

## Architecture

- **Framework**: Gatsby v3 with React
- **Styling**: styled-components with custom theme system
- **Content**: Markdown files in `content/` processed by Gatsby plugins
- **Data Flow**: Markdown → Gatsby nodes → React components → static HTML/CSS/JS

## Key Components

- **Layout**: [src/components/layout.js](src/components/layout.js) - wraps pages with theme provider, global styles, and navigation
- **Sections**: Modular components in [src/components/sections/](src/components/sections/) (Hero, About, Jobs, Featured, Projects, Contact)
- **Icons**: SVG components in [src/components/icons/](src/components/icons/) for consistent iconography
- **Navigation**: [src/components/nav.js](src/components/nav.js) with scroll-based highlighting

## Styling Patterns

- Use styled-components with theme breakpoints: `theme.bp.tabletL`, `theme.bp.desktopS`
- Mixins for common patterns: `theme.mixins.flexCenter`, `theme.mixins.inlineLink`
- CSS variables in [src/styles/variables.js](src/styles/variables.js) for colors (--navy, --green)
- Global styles in [src/styles/GlobalStyle.js](src/styles/GlobalStyle.js) handle fonts, focus, and resets

## Content Management

- Projects/posts in `content/projects/` and `content/posts/` as Markdown with frontmatter
- Images referenced relatively, processed by gatsby-plugin-sharp
- Featured work in `content/featured/` with custom templates

## Development Workflow

- **Start dev server**: `yarn develop` (serves at localhost:8000)
- **Build production**: `yarn build`
- **Format code**: `yarn format` (Prettier on JS/JSX/JSON/MD)
- **Lint**: ESLint via lint-staged on pre-commit
- **Clean cache**: `yarn clean` before builds if issues

## Conventions

- Import components with `@components` alias (configured in gatsby-config.js)
- Component files: PascalCase, one component per file
- Styled components: prefixed with `Styled` (e.g., `StyledContainer`)
- Props: Use PropTypes for validation
- Hooks: Custom hooks in [src/hooks/](src/hooks/) for reusable logic (useScrollDirection, usePrefersReducedMotion)

## Examples

- Adding a new section: Create component in sections/, import in [src/pages/index.js](src/pages/index.js), add to StyledMainContainer
- Styling responsive: Use theme breakpoints in media queries, e.g., `@media ${theme.bp.tabletL} { ... }`
- Content query: Use GraphQL in templates like [src/templates/post.js](src/templates/post.js) to fetch Markdown data</content>
  <parameter name="filePath">c:\Users\semih\OneDrive\Masaüstü\Portfolio\Portfolio\.github\copilot-instructions.md
