# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Stack & Conventions

**Hard constraint: vanilla HTML, CSS, and JavaScript only — no frameworks, no build step.**

- No frontend frameworks or libraries (no React, Vue, Svelte, jQuery, etc.).
- No build tools, bundlers, transpilers, or package managers (no webpack, Vite, esbuild, Babel, npm/yarn/pnpm install steps).
- No `node_modules`, no `package.json` dependencies for the app itself.
- Write plain `.html`, `.css`, and `.js` files that run directly in the browser with no compilation step.
- Use standard ES modules (`<script type="module">`) if code needs to be split across files — do not introduce a bundler to achieve this.
- Prefer native browser and Web APIs over third-party libraries.

## Writing Style

- Use a **bold lead-in** at the start of paragraphs where possible, to make paragraphs easier to scan and read.

## Tech stack (hard constraints — do not deviate)
- Vanilla HTML, CSS, and JavaScript only. No React, Vue, or any JS framework.
- Tailwind CSS for all styling (via CDN only).
- No backend, no database. Fully static site.
- A toggle for light and dark theme, with the choice remembered
  across visits.

## Outline & Visual Direction

- Single-page tool portal: header (title + theme toggle) on top, a left-hand nav listing available tools, and a main panel to the right.
- Clicking a nav item opens that tool's card in the main panel. Clicking the same nav item again (or the card's close button) closes it, returning the main panel to its empty state. Only one tool card is open at a time.
- Minimal look: neutral background, single accent color, generous spacing, no decorative chrome. Styled entirely with Tailwind utility classes.

## Feature Plan

- [x] Phase 1 — Shell & navigation: page scaffold, header with theme toggle (persisted via `localStorage`), nav with placeholder tool cards that open and close correctly.
- [ ] Phase 2 — Real tool logic: implement actual functionality behind each placeholder card.
- [ ] Phase 3 — Polish: refine styling, responsiveness, accessibility.
