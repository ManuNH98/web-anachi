# AGENTS.md

## Project Overview

This repository contains the public landing page for Aduanas Anachi, built with Astro, Tailwind CSS 4, and the Vercel adapter. It is a static Spanish-language marketing site focused on customs services in Las Palmas de Gran Canaria.

## Package Manager

Use `pnpm` only.

- Install dependencies with `pnpm install`.
- Run local development with `pnpm dev`.
- Build production output with `pnpm build`.
- Preview the built site with `pnpm preview`.
- Do not create or commit `package-lock.json`, `npm-shrinkwrap.json`, or `yarn.lock`.

## Tech Stack

- Astro 6 for pages, layouts, static rendering, and asset handling.
- Tailwind CSS 4 through `@tailwindcss/vite`.
- Vercel adapter through `@astrojs/vercel`.
- TypeScript configuration extends Astro strict defaults.

## Repository Structure

- `src/pages/index.astro`: Main page composition.
- `src/layouts/Layout.astro`: Base HTML document, metadata, canonical URL, Open Graph, Twitter card, and footer slot.
- `src/components/`: Page sections and shared UI components.
- `src/styles/global.css`: Global imports, CSS variables, base styles, and reusable component classes.
- `src/assets/`: Source images and logos imported by Astro components.
- `public/`: Static public assets served from the site root.
- `astro.config.mjs`: Astro, Tailwind Vite plugin, and Vercel adapter configuration.
- `tailwind.config.mjs`: Tailwind content configuration.

## Site Sections

- `Header.astro`: Desktop navigation, mobile menu, and primary contact CTA.
- `HeroSection.astro`: Main hero with background image and lead CTA.
- `SocialSection.astro`: Trust counters and capability message.
- `ServiceSection.astro`: Customs service cards.
- `AboutSection.astro`: Company story, credentials, and team members.
- `ContactSection.astro`: Contact details, Formspree form, and FAQ accordion.
- `Footer.astro`: Logo, navigation, address, email, phone, and LinkedIn link.

## Development Guidelines

- Keep content in Spanish unless the user requests another language.
- Preserve the current visual identity: dark navy, orange accent, white cards, Montserrat headings, and Lato body text.
- Prefer small, direct changes in the existing Astro components instead of introducing new abstractions.
- Import image assets from `src/assets` when they need Astro optimization or dimensions.
- Use `public/` only for files that must be addressed by a stable root URL, such as `/favicon.svg`.
- Keep IDs and navigation anchors aligned. Current primary anchors are `#home`, `#services`, `#about-us`, and `#contact`.
- Avoid adding client-side JavaScript unless static HTML/CSS or existing inline scripts are insufficient.
- Before finishing code changes, run `pnpm build`.

## Deployment Notes

- Production output is generated in `dist/`.
- Vercel build output may be generated in `.vercel/` during builds.
- Both `dist/` and `.vercel/` are generated artifacts and should not be committed.

## Known Content Notes

- The contact form posts to Formspree. Confirm the endpoint before production changes.
- Contact information appears in both `ContactSection.astro` and `Footer.astro`; keep them synchronized when editing.
