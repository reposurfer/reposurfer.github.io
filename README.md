# reposurfer.github.io

Personal portfolio site, built with Vue, TypeScript, Tailwind CSS, and PrimeVue. The site is intentionally small: a single-page profile with intro copy, experience, project links, and contact links.

## Tech Stack

- [Vue 3](https://vuejs.org/) with `<script setup>`
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vite.dev/) for local development and production builds
- [Tailwind CSS](https://tailwindcss.com/) for utility-first styling
- [PrimeVue](https://primevue.org/) for UI primitives
- [Vue Router](https://router.vuejs.org/) for route structure

## Project Structure

```text
src/
  assets/
    main.css
  components/
    home/
      HomeExperienceList.vue
      HomeHighlightLink.vue
      HomeIntro.vue
      HomeProjectList.vue
      HomeSidebar.vue
      HomeSidebarSection.vue
  router/
    index.ts
  views/
    HomeView.vue
  App.vue
  main.ts
```

## Getting Started

Install dependencies:

```sh
npm install
```

Start the local development server:

```sh
npm run dev
```

Build for production:

```sh
npm run build
```

Preview the production build locally:

```sh
npm run preview
```

## Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite dev server. |
| `npm run build` | Type-check and build the app into `dist/`. |
| `npm run build-only` | Build the app without running the type checker. |
| `npm run type-check` | Run `vue-tsc` against the project. |
| `npm run lint` | Run Oxlint and ESLint with auto-fix enabled. |
| `npm run format` | Format source files with `oxfmt`. |
| `npm run preview` | Serve the built `dist/` output locally. |

## Deployment

The project includes a GitHub Pages workflow at `.github/workflows/deploy.yml`. On pushes to `main`, GitHub Actions installs dependencies, runs `npm run build`, uploads `dist/`, and deploys it to GitHub Pages.

## Requirements

The project expects Node.js compatible with:

```text
^20.19.0 || >=22.12.0
```

Using `npm ci` is recommended in CI because the project includes a `package-lock.json`.
