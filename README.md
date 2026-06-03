# Liel Mazar — Portfolio

Personal portfolio site for Liel Mazar, an independent technical and regulatory
consultant. It is a single-page, static website built with plain HTML and CSS
(plus a few lines of vanilla JavaScript for the theme toggle and footer year).

**Live site:** https://portfolio.cservices.co.il/

## What it is

A clean, fast, responsive one-pager covering About, Focus areas, Selected
projects, Publications & activities, and Contact. There is **no build step and no
framework** — GitHub Pages serves the files directly from the repository root on
the `main` branch.

## Project structure

```
.
├── index.html      # the entire page
├── styles.css      # all styling (mobile-first, light/dark)
├── assets/         # favicon and social/Open Graph image
│   ├── favicon.svg
│   ├── favicon.png
│   └── og-image.png
├── CNAME           # custom domain for GitHub Pages: portfolio.cservices.co.il
├── .nojekyll       # tells Pages to skip Jekyll processing
├── README.md
└── LICENSE         # MIT
```

## Run locally

No tooling required — it works offline. Either:

- Double-click `index.html` to open it directly in a browser, **or**
- Serve it locally (nicer for testing relative paths):

  ```bash
  # Python 3
  python3 -m http.server 8000
  # then open http://localhost:8000
  ```

## Edit content

All text lives in `index.html`, organized into clearly labelled `<section>`
blocks (hero, about, focus, projects, publications, contact). Edit the markup
directly. Styling is in `styles.css`; the colour palette is defined once as CSS
custom properties (`:root`) near the top, with a dark-theme override.

To replace the monogram with a photo later: add the image to `assets/`, then
swap the `.hero__avatar` monogram in `index.html` for an `<img>` with descriptive
`alt` text.

## How GitHub Pages is set up

- **Source:** Deploy from a branch → branch `main`, folder `/` (root).
- **Custom domain:** `portfolio.cservices.co.il`, stored in the `CNAME` file.
- **HTTPS:** "Enforce HTTPS" is enabled once GitHub provisions the certificate.
- **DNS:** a `CNAME` record for the `portfolio` subdomain of `cservices.co.il`
  points to `lielmazar.github.io`.

After pushing to `main`, GitHub Pages redeploys automatically.

## License

[MIT](LICENSE) © 2026 Liel Mazar.
