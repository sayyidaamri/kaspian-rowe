# KASPIAN.ROWE — portfolio (native HTML)

<p align="center"><img src="docs/preview/homepage.gif" alt="Homepage preview — full-page scroll" width="100%"></p>

An original site for a fictional
systems & AI engineer, **Kaspian Rowe** (monogram **KR**, Bergen, Norway). Plain HTML/CSS/JS, no framework,
no build step needed to view it.

## Open it

Double-click `index.html` (works from `file://`, offline). Everything — fonts, images, scripts — is local.
Tested in Chromium/Edge; any modern browser works.

## Structure

This folder is the finished static site. Upload it as-is to any static host.

```
index.html                   home
projects.html                project index (search + language filter)
project/<slug>.html          11 case studies
lab.html                     components dissected + 4 experiments
cv.html                      resume (Print / Download PDF → browser print dialog)
privacy-policy.html, legal-notice.html, 404.html
assets/css/style.css         all styles (tokens at the top)
assets/js/app.js             chrome & interactions (preloader, smooth scroll, cursor, menu, cookies, stars…)
assets/js/fx.js              canvas/WebGL effects (dither hero, globes, service canvases, pixel images, diagrams)
assets/js/lab.js             lab experiments (Gray-Scott, type as matter, flow field, ASCII globe)
assets/js/chat.js            local assistant (no network)
assets/js/landmask.js        world land mask (Natural Earth, public domain)
assets/js/thumbs.js          small grayscale copies of the photos (lets canvas dithering work from file://)
assets/img/                  Unsplash photos
assets/art/                  generated art (ridge lines, noise band, halftone globe)
assets/fonts/                Big Shoulders Display, Geist, Geist Mono, Unbounded (SIL OFL) + fonts.css
```

Case studies (`project/`): halvorsen-marine, tidewatch, ledgerly, fjordline-institute, fjordline-archive,
skills-atlas, wrist-folio, gull-quest, saltmarket, taskharbor, echo-radio.

## Editing

The HTML pages in this folder are generated output; the generator (`build/`: `data.mjs`, `build.mjs`, and the
`art.py` / `thumbs.py` / `landmask.py` helpers) is **not** included here. Edit the HTML, CSS and JS directly.
Keep these in sync by hand when you change them:

- Copy that repeats on every page (header, footer, brand name, email, social links).
- `assets/js/thumbs.js` — if you add or replace a photo in `assets/img/`, its grayscale thumbnail must be
  regenerated, otherwise the dither effect won't pick it up from `file://`.

## States & easter eggs to try

- Preloader (first visit per tab) and curtain transitions between pages.
- Assistant (bottom-right): open, ask, minimise, reset, close.
- Cookie banner: Accept / Decline; reopen with “Manage cookies” in the footer.
- Three hidden ★ (hero info bar, contact form header, footer) → unlocks the StarGame.
- Konami code ↑↑↓↓←→←→BA (or 5 taps on “KR” on mobile) → negative mode.
- Mobile: Menu, “Read more” pixel expander, horizontal card rows.
- Contact form validation (demo only — nothing is sent).

## Placeholders to replace

Name/brand, email `hello@kaspianrowe.dev`, phone, GitHub/LinkedIn URLs, all project names/clients (fictional),
“View site / View code” links (`#`), the resume content (`cv.html`). Search the HTML files for `kaspianrowe`
and `Kaspian` to find every occurrence.
