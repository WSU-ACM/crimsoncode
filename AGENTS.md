# Repository Guide

## Structure

- This is a GitHub Pages static site, not a package-managed app. The entire site, including styles and behavior, is in `index.html`.
- `cch26-vert-poster.pdf` is the only tracked local site asset. Most images, Google Fonts, and Tailwind CSS are loaded from external CDNs.
- There is no build, test, lint, format, or deployment configuration in this repository. Do not introduce package-manager steps when a direct HTML/CSS/JavaScript edit is sufficient.

## Local Verification

- Preview from the repository root with `python3 -m http.server 8000`, then open `http://localhost:8000/`.
- Check both desktop and mobile widths after changing layout or interactions. Also exercise the hidden-on-load header, mobile menu, FAQ accordion, track-card flip, hero slideshow, and scroll animations when relevant.
- Use the browser console and network panel: core presentation depends on remote CDN resources, so opening the file or testing offline is not representative.

## Editing Notes

- Keep section IDs in sync with desktop/mobile navigation links and in-page links.
- Event details are repeated across the title, hero, FAQ, schedule, links, and MLH badge; search the full `index.html` when changing a year, date, status, or registration/project URL.
- Tailwind is loaded through `https://cdn.tailwindcss.com`; classes are interpreted in the browser rather than compiled locally.
