# Shubham Kumar — Portfolio

Personal portfolio site for **Shubham Kumar** — Customer Experience Specialist moving into business analytics. Based in Patna, India.

**Live:** https://shubhamrajsen.github.io/

## Stack

Single-file static site — no build step, no dependencies.

| Concern | Implementation |
|---|---|
| Markup / styles / behaviour | `index.html` (self-contained) |
| Typography | Cormorant Garamond + DM Sans (Google Fonts) |
| Contact form | [Formspree](https://formspree.io/f/mlgpbrak) — serverless POST |
| Hosting | GitHub Pages (`main` branch, root) |

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Accessibility

- Custom cursor is scoped to `@media (hover: hover) and (pointer: fine)`, so touch devices keep the native pointer and the animation loop never starts on them.
- All animation and reveal transitions collapse under `prefers-reduced-motion: reduce`.
- Form fields use real `<label for>` associations and report send status via `aria-live="polite"`.
- Mobile navigation is a proper `aria-expanded` drawer with Escape-to-close, replacing the previous version where nav links simply vanished below 900px.

## Before you deploy — two files to add

Both are referenced in `index.html` but **commented out**, so the live site serves no dead links in the meantime. Add the file, then uncomment the matching line.

1. **`headshot.jpg`** — drop a professional photo at the repo root and uncomment the `<img class="hero-photo">` in the hero. It covers the "SK" monogram automatically (`.hero-photo` is absolutely positioned over the placeholder).
2. **`Shubham-Kumar-Resume.pdf`** — uncomment the hero's "Download Résumé" button.

These were originally wired up unconditionally, but `GET /headshot.jpg` returned **HTTP 404** — meaning every visitor's console logged an error and wasted a request until the photo existed. Commenting them out removes that.

## Copy policy

Every metric on this page is either a maintained operating level (90%+ first-contact resolution) or a plain count (3 years, 6 certifications). Earlier drafts carried repeated round percentages — 25% / 20% / 15% — across both job roles *and* the Castrol project, which read as invented rather than measured. If you add a figure back, give it a denominator and a baseline, e.g. `CSAT 4.1 → 4.8 across ~180 tickets/month`.

## Roadmap

- [ ] Add `headshot.jpg`
- [ ] Add `Shubham-Kumar-Resume.pdf`
- [ ] Add Power BI dashboard screenshots to the Sales Performance project
- [ ] Add an Open Graph preview image for social sharing
- [ ] Flesh out `powerbi-sales-report` (currently a 317-byte README)

## License

© 2025 Shubham Kumar. All rights reserved.
