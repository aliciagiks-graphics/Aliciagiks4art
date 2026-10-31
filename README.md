# Aliciagiks4art

A creative portfolio for Mary Alicia, featuring graphic design, illustration, animation, motion design, and digital experiences.

## Overview

The site brings selected visual work together in a responsive portfolio with project filters, search, image and video previews, service information, an artist profile, and direct contact links. Artwork and video are stored in `public/` and the project catalogue is maintained in `src/data/portfolioData.ts` and `public/geeks4drisony/manifest.json`.

## Tech stack

- React and TypeScript
- Vite
- Tailwind CSS
- Motion for interface animation
- Lucide icons
- Static site output for Cloudflare Pages

## Project structure

```text
.
├── index.html
├── src/
│   ├── App.tsx
│   ├── index.css
│   ├── components/
│   └── data/portfolioData.ts
├── public/
│   ├── assets/
│   └── geeks4drisony/
│       ├── manifest.json
│       └── project artwork and video
├── package.json
├── vite.config.ts
└── wrangler.jsonc
```

## Run locally

Install [Bun](https://bun.sh), then run:

```bash
bun install
bun run dev
```

Vite serves the local preview at the address printed in the terminal.

## Deploy to Cloudflare Pages

Connect the `aliciagiks-graphics/Aliciagiks4art` repository to Cloudflare Pages and use:

- Production branch: `main`
- Framework preset: `None`
- Build command: `bun run build`
- Build output directory: `dist`
- Root directory: `/`

`wrangler.jsonc` also sets `pages_build_output_dir` to `dist`. Keep the dashboard output directory and this setting in sync. The build command is required because the browser cannot run the TypeScript and React source files directly; Vite compiles them into the static files in `dist/`.

## Customize

- Edit the introduction and portfolio presentation in `src/components/`.
- Update featured projects, services, and artist information in `src/data/portfolioData.ts`.
- Add artwork and video under `public/geeks4drisony/`, then update `public/geeks4drisony/manifest.json` to include new work in the archive.
