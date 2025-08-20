# Copilot Instructions for Portfolio Website

## Project Overview
This is a static portfolio website built with HTML and SCSS. The main entry point is `index.html`, which references compiled CSS from SCSS sources in `assets/scss/`.

## Architecture & File Structure
- `index.html`: Main HTML file. Contains sections for Home, About, Resume, Work, Testimonial, and Contact.
- `assets/scss/`: Contains modular SCSS files for each section and a `main.scss` that imports them.
    - Example: `_home.scss` styles the `#home` section.
- `assets/css/main.css`: Compiled CSS output from SCSS. Do not edit directly; always update SCSS files.

## Developer Workflow
- **Edit styles in SCSS files** (`assets/scss/`).
- **Compile SCSS to CSS**: Use a SCSS compiler (e.g., `sass assets/scss/main.scss assets/css/main.css`).
    - On Windows PowerShell: `sass assets/scss/main.scss assets/css/main.css`
- **Preview changes** by opening `index.html` in a browser.

## Patterns & Conventions
- Each section in HTML (`#home`, `#about`, etc.) has a corresponding SCSS partial (`_home.scss`, `_about.scss`, etc.).
- All partials are imported in `main.scss` using `@import`.
- Section backgrounds are set in their respective SCSS files (see `_home.scss`, `_work.scss`, `_contact.scss`).
- Empty SCSS files indicate sections ready for future styling.

## Integration Points
- No JavaScript or external frameworks are present.
- No build scripts or package managers detected; manual SCSS compilation is expected.

## Example: Adding a New Section
1. Add a `<section id="newsection">` to `index.html`.
2. Create `_newsection.scss` in `assets/scss/` and add styles.
3. Add `@import "./newsection";` to `main.scss`.
4. Recompile SCSS to CSS.

## Key Files
- `index.html`: Structure and content.
- `assets/scss/main.scss`: SCSS entry point.
- `assets/css/main.css`: Output CSS.

---
For questions or unclear conventions, ask for clarification or review the structure above.
