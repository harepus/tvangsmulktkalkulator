# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A small static Norwegian tax penalty calculator site (`index.html` plus article pages) for "tvangsmulkt" — daily fines levied by Skatteetaten (Norwegian Tax Administration) for late filing of mandatory reports. No build system, no dependencies, no package manager.

## Development

Open `index.html` directly in a browser, or run `python3 -m http.server` for root-relative links to work. Deployed on Cloudflare Pages (push to `main` deploys).

## Architecture

- **`styles.css`**: shared by every page. Palette tokens (`--paper`, `--ink`, `--stamp`, ...), Schibsted Grotesk, site header/nav, article components (`.card` tables, `.tip`, `.warn`, `.steps`, `.related`), and calculator components (`.box` fields, `.seg` ENK/AS switch, `.slip` result with meter).
- **`index.html`**: calculator. JS has the rate table `T` (daily rate `r`, cap `m`, employee multiplier `e`), `DESC`/`WHO` help texts (WHO is per business type: `enk`/`as`), and `c()` which recalculates on every input.
- **Articles**: `tvangsmulkt-guide.html`, `klage-tvangsmulkt.html`, `frister-2026.html`, `rettsgebyr-2026.html`. The site header/nav and footer links are duplicated in each page; update all of them when adding a page (and `sitemap.xml`).
- **`frister-2026.html`**: deadline cells carry `data-due="YYYY-MM-DD"` (the effective date after weekend moves); a small script adds "passert"/"neste frist" badges, so nothing needs hand-updating during the year.
- **`404.html`**: makes Cloudflare Pages return real 404s instead of serving the homepage for unknown URLs.
- **`og-image.png`, `apple-touch-icon.png`**: rendered from HTML with Playwright; `favicon.svg` is the source mark.

## Rate table structure

```js
var R = 1345; // rettsgebyr (court fee base) for 2026
var T = {
  mva:       { r: R*0.5, m: R*50,   e: 0 },           // half rettsgebyr/day, cap 50x
  amelding:  { r: R*0.1, m: R*1000, e: 1, el: "..." }, // per-employee multiplier
  otp:       { r: 250,   m: Infinity,e: 1, el: "..." }, // fixed rate, no cap
  bokforing: { r: R*1,   m: 1e6,    e: 0 },             // full rettsgebyr/day
  // ...
};
```

When updating rates for a new year, change `R` in `index.html`, the hardcoded amounts in the article pages and `rettsgebyr-2026.html`, the `data-due` dates in `frister-2026.html`, and adjust per-type overrides as needed. The `rettsgebyr` value is set annually by the Norwegian government.

## Locale

All user-facing text is Norwegian Bokmal. Numbers use `toLocaleString("nb-NO")` for Norwegian formatting (space as thousands separator, comma as decimal).
