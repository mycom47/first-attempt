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
