# Newlife — Project Overview

## What the project has today

### Files & structure

| File | Purpose |
|------|---------|
| `index.html` | Home page with sidebar navigation and main content |
| `about.html` | Dedicated About page, linked from the home page |
| `styles.css` | Shared layout and sidebar styling |
| `overview.md` | This document — project inventory and improvement notes |
| `README.md` | Minimal repo title stub |

### Features

- **Sidebar navigation** — Five buttons: Home, About, Projects, Contact, Overview
- **Multi-page setup** — Home and About are separate HTML pages
- **Anchor links** — Home page includes a link to the About page; sidebar buttons use in-page anchors where pages do not exist yet
- **Responsive layout** — Sidebar stacks horizontally on small screens
- **Dark theme** — Simple, readable color palette in `styles.css`

### Tech stack

- Plain HTML5
- CSS (no framework)
- No build step, bundler, or package manager
- Git repository initialized under `newlife/`

---

## Structural improvements

### Short term

1. **Shared layout component** — Sidebar markup is duplicated in each HTML file. Extract into a small include pattern (e.g. a static site generator, or a single-page app) to avoid drift.
2. **Consistent page titles and meta** — Add description, Open Graph, and favicon tags to every page.
3. **Folder organization** — Consider:
   ```
   newlife/
   ├── index.html
   ├── pages/
   │   └── about.html
   ├── assets/
   │   └── css/
   │       └── styles.css
   └── docs/
       └── overview.md
   ```
4. **Placeholder pages** — Projects and Contact currently point to `#` anchors on the home page. Create real pages or remove dead links.
5. **Expand README** — Document how to open/run the site locally and what each file does.

### Medium term

1. **Static site generator or framework** — As pages grow, tools like Vite, Eleventy, or Astro reduce duplication and improve maintainability.
2. **Component reuse** — Navbar, footer, and layout wrapper should live in one place.
3. **Asset pipeline** — Minify CSS, optimize images, and add a simple deploy script.
4. **Testing** — Link checker or basic HTML validation in CI.
5. **Accessibility audit** — Skip links, focus states, ARIA labels, and keyboard navigation review.

### Long term

1. **Backend or CMS** — If content will change often, add a headless CMS or lightweight API.
2. **Authentication** — Only if user accounts or private areas are needed.
3. **Internationalization** — Multi-language support if the audience grows.
4. **Analytics & SEO** — Structured data, sitemap, and privacy-conscious analytics.

---

## Feature improvements

### Content & pages

- [ ] **Projects section** — Showcase work with cards, tags, and links to demos/repos
- [ ] **Contact form or links** — Email, social profiles, or a simple form
- [ ] **Blog or updates** — Chronological posts for progress logs
- [ ] **404 page** — Friendly error page for broken links

### UX & design

- [ ] **Active nav state** — Already on About; ensure all pages highlight the current section
- [ ] **Mobile menu** — Collapsible sidebar or hamburger on very small screens
- [ ] **Light/dark toggle** — Optional theme switcher
- [ ] **Animations** — Subtle page transitions without hurting performance
- [ ] **Typography scale** — Consistent heading sizes and spacing tokens

### Developer experience

- [ ] **`package.json`** — Scripts for local dev server (`npx serve` or `vite`)
- [ ] **Linting** — HTML/CSS formatters (Prettier) and optional ESLint for any JS
- [ ] **Git hooks** — Pre-commit checks for formatting
- [ ] **Deploy target** — GitHub Pages, Netlify, or Vercel with one-click deploy from `main`

---

## Suggested next steps

1. Flesh out the **Projects** and **Contact** sections on the home page or as new pages.
2. Add a **footer** with copyright, repo link, and last-updated date.
3. Set up a **local dev server** and document it in `README.md`.
4. Choose a **deploy platform** and add a workflow so the site is live on every push.

---

## Summary

Newlife is an early-stage static website with a sidebar, a home page, an About page, shared CSS, and project documentation. The foundation is in place; the biggest wins ahead are reducing duplicated HTML, filling in placeholder navigation targets, and adding a minimal toolchain for development and deployment.
