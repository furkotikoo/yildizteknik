# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website for **Yıldız Teknik**, a local home/business repair service in Batman, Turkey. No build system, no package manager, no server-side code — all files are served directly as static assets.

## Development

Open any `.html` file directly in a browser, or serve locally:

```bash
python3 -m http.server 8080
```

There are no build, lint, or test commands.

## Architecture

### Pages
| File | Purpose |
|---|---|
| `index.html` | Homepage with hero carousel, services overview, facts, team |
| `service.html` | Full service catalog |
| `feature.html` | Feature highlights |
| `about.html` | Company background |
| `team.html` | Team members |
| `testimonial.html` | Customer reviews |
| `appointment.html` | Appointment booking form |
| `contact.html` | Contact form and map |
| `404.html` | Error page |

### Styles
- `css/style.css` — custom styles; CSS variables define the color palette (`--primary: #fda12b`, `--secondary: #8d9297`, `--dark: #182333`)
- `scss/bootstrap.scss` — customized Bootstrap variable overrides (same palette as CSS vars); compiled output goes to `css/bootstrap.min.css`
- `lib/` — vendored third-party libraries: Bootstrap, Animate.css, easing, OwlCarousel, Waypoints, WOW.js

### JavaScript
- `js/main.js` — single JS file; initializes OwlCarousel, WOW.js, back-to-top button, spinner, and sticky navbar

### Tracking
Every page includes the Google Ads tag `AW-18034155714` in `<head>` via `gtag.js`. When adding new pages, copy this block from an existing page.

### SEO / Schema
`index.html` includes a `LocalBusiness` JSON-LD schema block with business address, phone, and hours. Other pages include page-specific meta tags in Turkish.

## Key Details

- Language: Turkish (`<html lang="tr">`)
- Phone: +90 532 559 83 82
- Address: Çamlıtepe, 4063. Sk. No:14, Batman Merkez, 72000
- Instagram: `@yildizteknik_72`
- Business hours: Mon–Sun 08:00–20:00
- All images live in `img/`; use the existing naming convention (service name in Turkish, kebab-case)
