# Copilot / AI agent instructions for Nomada_food

This repository is a small static website for "Nómada Food". The goal of this file is to provide concise, actionable guidance so an AI coding assistant can be productive immediately.

Summary (big picture)
- Type: Static HTML/CSS prototype (single-page). Main artifacts: `index.html`, `css/style.css`, `images/`, `icons/`.
- Purpose: simple marketing/footer prototype. No build system, no JS, and no server-side code discovered.

What to modify and why
- `index.html` contains the page markup. Changes commonly target the footer section (class `footer-content`) and the logo image at `images/logo.png`.
- `css/style.css` contains styling. It currently contains non-standard CSS comments and a few syntactic issues (see examples below).

Project-specific patterns and notes
- Files are root-level, not organized into `src`/`dist`. Keep edits simple and relative (e.g., `css/style.css`, `images/logo.png`).
- Use Spanish copy for visible text (the page is `lang="es"`). Align translations accordingly when editing content.
- Minimal responsive layout: footer uses `.footer-content` with `display:flex; flex-direction:column; align-items:center;` — prefer small changes that preserve the vertical center alignment.

Concrete examples & fixes to demonstrate patterns
- CSS issues found in `css/style.css`:
  - The file starts with plain text `Estilos para footer` (not a valid CSS comment). Replace with `/* Estilos para footer */`.
  - Property `justify-content: Center;` should be `center` (lowercase).
  - `margin.bottom: 10px;` is invalid — use `margin-bottom: 10px;`.
  - Color contrast: footer background `#222` and text color `#0b0a0a` are both very dark; when updating copy ensure sufficient contrast.

Developer workflows
- There is no build step detected. Editing files directly and previewing `index.html` in the browser is the main workflow.
- Tests: no automated tests discovered.
- Debugging: for CSS/HTML issues, open `index.html` in a browser and use devtools (Elements/Inspector) to validate layout and styles.

Conventions and style
- Keep markup and class names minimal and semantic. Footer uses `.footer-content` and `.logo` — prefer reusing these rather than introducing many new classes.
- Keep Spanish copy consistent (e.g., `Contacto`, `Fabricación`). If adding new copy, place it in Spanish by default.

Integration & dependencies
- No external dependencies or package manifests were found. All assets are local.
- External links in `index.html` point to third-party sites (e.g., `uniremington.com`). Do not change these without instruction.

What an AI assistant can safely do
- Fix obvious HTML/CSS syntax bugs (examples above).
- Improve accessibility (add `alt` text to images — already present — and ensure semantic footer markup, e.g., include a `<div role="contentinfo">` if needed).
- Suggest small, low-risk UX improvements: increase text contrast, add link target attributes (`rel="noopener" target="_blank"`) for external links.

What to avoid or ask before changing
- Rework of project structure (moving to `src/` or adding a build system) without the user's approval.
- Changing copy or external links without confirmation.

Quick patch example (what to change first)
- In `css/style.css`: replace the top line with a proper comment and fix the invalid properties listed above.

If you need clarification
- Ask whether the user wants a full responsive footer rewrite or only small fixes.
- Ask if new assets or languages should be added.

Please review this file and tell me if you'd like me to apply the safe fixes I listed (CSS cleanup + minor accessibility tweaks).