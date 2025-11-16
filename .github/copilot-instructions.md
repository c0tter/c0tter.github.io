<!-- Project-specific Copilot instructions for editing: c0tter.github.io (Poynton Round Table static site) -->
# Copilot instructions — Poynton Round Table static site

Keep edits minimal, predictable, and safe. This repository is a plain static website (root-level .html pages + `assets/` for CSS/media`) — there is no build system or server-side app.

Quick facts
- This is a static site: top-level HTML files (e.g. `index.html`, `events.html`, `donations.html`) and `assets/css/style.css`.
- Navigation uses absolute paths (e.g. `/events.html`, `/contact-us.html`). Prefer updating the files referenced by those links rather than similarly-named duplicates.
- There are multiple files with inconsistent naming/capitalisation (for example `Events.html` and `events.html`, `Donations.html` and `donations.html`, `Contact us.html` and `contact-us.html`). Treat the lowercase/hyphenated files referenced from `index.html` as canonical. Do not rename or delete other files without explicit confirmation from a human.

When editing HTML
- Preserve the simple, semantic structure used across pages: header with `.site-header`, `.container`, nav links, main content and `.site-footer`.
- Keep CSS class names as-is (examples: `.hero`, `.hero-copy`, `.grid`, `.card`, `.events-list`). Avoid introducing a new naming scheme.
- Use existing assets path: reference CSS at `/assets/css/style.css` and keep any new media under `assets/`.
- Avoid changing filenames that contain spaces or unconventional punctuation (e.g. `Photo Galley.html`, `Poynton Round Table _Registered Charity_.html`) unless user explicitly requests a rename — these may be kept for historical reasons.

Content and copy edits
- Prefer in-place copy updates in the canonical HTML files (`index.html`, `events.html`, `donations.html`, `contact-us.html`, `about-us.html`).
- If adding links, use the existing hyphenated-lowercase / root-relative convention (e.g. `/donations.html`).
- When adding or editing lists (e.g. `.events-list`), keep markup simple (ul/li) and avoid adding client-side JS unless requested.

Preview and testing
- There is no build step. To preview locally, serve the repo root with a static server (for example: `python3 -m http.server 8000` from the repo root) and open `http://localhost:8000/`.

Examples from the repo
- Header & nav (see `index.html`): uses `.site-header` / `.header-inner` and links to `/events.html` and `/contact-us.html`.
- Main hero (see `index.html`): `.hero`, `.hero-copy`, `.hero-media`, and CTA buttons `.btn.primary` / `.btn.outline`.
- Styles (see `assets/css/style.css`): theme variables in `:root`, container width in `.container`, responsive breakpoint at `@media (max-width:880px)`.

Do not do without asking
- Bulk rename or remove files (especially those with different capitalisation or spaces).
- Move the site into a different build tool or framework without prior approval.

If uncertain, ask the human reviewer which file is canonical before making disruptive changes.

Thanks — keep changes small and verifiable.
