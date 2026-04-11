# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A single-file Norwegian tax penalty calculator (`index.html`) for "tvangsmulkt" — daily fines levied by Skatteetaten (Norwegian Tax Administration) for late filing of mandatory reports. No build system, no dependencies, no package manager.

## Development

Open `index.html` directly in a browser — no server required. All logic, styles, and markup live in the one file.

## Architecture

Everything is in `index.html`:

- **CSS** (inline `<style>`): CSS custom properties for the color palette (`--bg`, `--accent`, etc.), responsive grid layout, card/result components.
- **HTML**: Calculator form (report type selector + days/employees inputs), result display card, informational sections (deadlines, appeal info), footer.
- **JS** (inline `<script>`): Rate table `T` keyed by report type, each entry with daily rate `r`, max cap `m`, and whether an employee-count multiplier applies `e`. The `c()` function recalculates on every input change and updates the DOM directly.

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

When updating rates for a new year, change `R` and adjust per-type overrides as needed. The `rettsgebyr` value is set annually by the Norwegian government.

## Locale

All user-facing text is Norwegian Bokmal. Numbers use `toLocaleString("nb-NO")` for Norwegian formatting (space as thousands separator, comma as decimal).
