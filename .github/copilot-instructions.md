# Copilot Instructions for adguard-wiki

## Project Overview
- This is a documentation site for AdGuard products, using [Docusaurus](https://docusaurus.io/) as the static site generator.
- Documentation is organized by product in `docs/`, with subfolders for each AdGuard product (e.g., `adguard-for-windows/`, `adguard-for-mac/`, etc.).
- Internationalization (i18n) is supported via the `i18n/` directory, with subfolders for each language.
- The site is configured via `docusaurus.config.js`, with navigation in `sidebars.js`.

## Key Workflows
- **Install dependencies:** Use `pnpm install` (pnpm is required).
- **Start local dev server:** `pnpm start` (serves docs at http://localhost:3000/).
- **Build static site:** `pnpm build` (outputs to `build/`).
- **Translate content:** Use Crowdin integration (`crowdin.yml`), and edit files in `i18n/` for manual changes.

## Project Conventions
- All documentation is in Markdown (`.md`).
- Each product section in `docs/` has a `_category_.json` for sidebar grouping.
- Use relative links for cross-references between docs.
- Images and static assets go in `static/` (referenced as `/img/...`).
- Custom rules for markdownlint are in `markdownlint-custom/`.
- Do not edit generated translation files in `i18n/` directly unless necessary.

## Patterns & Examples
- To add a new product or section, create a new folder in `docs/` and update `sidebars.js`.
- For new features or troubleshooting guides, add to the appropriate `features/` or `solving-problems/` subfolder.
- Example: To add a new "installation" guide for a product, add `installation.md` in the relevant product folder.

## Integration Points
- Crowdin for translations (see `crowdin.yml`).
- Docusaurus plugins and themes configured in `docusaurus.config.js`.

## References
- Main config: `docusaurus.config.js`
- Sidebar/nav: `sidebars.js`
- Build/test: `package.json`, `pnpm` scripts
- Linting: `markdownlint-custom/`

## AI Agent Guidance
- Follow existing folder and file naming conventions.
- When in doubt, mirror the structure of existing product folders.
- Reference `README.md` for project overview (if present).
- Ask for clarification if a workflow or convention is unclear.
