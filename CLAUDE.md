# CLAUDE.md — Project Context for Currency by Age

## What This Project Is

An interactive illustrated essay based on the viral sketch "Principal Currencies by Age" — the idea that what people value most (their "currency") shifts at every life stage:

| Age | Currency | Core Idea |
|-----|----------|-----------|
| 1 yr | Blocks | The first economy — stacking, hoarding, knocking down |
| 5 yrs | Cookies | The first medium of exchange — good behavior has a price |
| 16 yrs | Car Rides | Freedom = whoever has the car keys |
| 25 yrs | Lattes | Every meeting, crisis, and friendship starts with coffee |
| 31 yrs | Sleep | Would trade anything for 8 uninterrupted hours |
| 45 yrs | Actual Money | Mortgages, college funds, retirement — the real thing |
| 61 yrs | Time | The final currency — can't earn it back |

The same concept is presented in **four distinct editorial design styles**, each as a self-contained HTML file.

## File Structure

```
currency-by-age/
├── index.html          # NYTimes edition (default/homepage)
├── wsj.html            # Wall Street Journal edition
├── newyorker.html      # The New Yorker edition
├── economist.html      # The Economist edition
├── README.md           # Public-facing project documentation
├── CLAUDE.md           # This file — project context for Claude
└── .github/
    └── workflows/
        └── pages.yml   # GitHub Pages deployment workflow
```

## Architecture & Tech Decisions

- **Zero dependencies** — each page is a single self-contained HTML file with inline CSS and inline JS. No build tools, no frameworks, no bundlers.
- **Google Fonts** are the only external resource (loaded via CDN).
- **SVG illustrations** are all hand-crafted inline SVGs — no image files.
- **Canvas charts** are used in the Economist edition for data visualizations.
- **Intersection Observer API** powers all scroll-triggered animations across all editions.
- All pages are fully responsive with mobile breakpoints.

## Design Style Guide per Edition

### index.html — New York Times
- **Fonts:** Playfair Display (headlines), Libre Baskerville (body), Libre Franklin (UI)
- **Layout:** Full-viewport scroll-driven sections, two-column grid alternating text/illustration sides
- **Key elements:** Reading progress bar, auto-hiding topbar, chapter nav dots, dark interlude block, pull quotes with black left border
- **Color:** Nearly monochrome — black, white, grays, one muted blue accent (#567B95)
- **Interactive:** "What's Your Currency?" age input with result card and life-stage progress bar

### wsj.html — Wall Street Journal
- **Fonts:** Source Serif 4 (headlines), Inter (body/data)
- **Layout:** Three-column (stipple illustration | article | "By the Numbers" sidebar)
- **Key elements:** Scrolling stock ticker header (BLKS, COOK, RIDE, LATT, SLEP, USD, TIME), stipple-dot SVG illustrations mimicking hedcut style, data sidebars with statistics
- **Color:** Black, white, WSJ tan/cream (#F4EFEB), green/red for market indicators
- **Interactive:** Portfolio Builder with age slider and canvas donut chart showing currency allocation

### newyorker.html — The New Yorker
- **Fonts:** Playfair Display italic (masthead), Lora (body), Nunito Sans (UI)
- **Layout:** Single narrow column (~620px), classic magazine reading format
- **Key elements:** Red (#E52B2B) masthead bar, line-art cartoon SVGs with dry caption underneath, drop caps, dinkus dividers (three dots), generous whitespace
- **Color:** White, black, New Yorker red sparingly
- **Interactive:** "Letters to the Editor" — enter age, get a personalized New Yorker cartoon caption

### economist.html — The Economist
- **Fonts:** Zilla Slab (headlines), Merriweather (body), Source Sans 3 (UI/data)
- **Layout:** Two-column article sections, data table at top
- **Key elements:** Red (#E3120B) top bar, punny headlines with red left border, 7 canvas-rendered charts (bar, line, area, stacked area), Global Currency Index ranking table, no bylines
- **Color:** Economist red, dark navy (#1D2B35), charcoal, light gray (#F6F6F6)
- **Interactive:** "Economist Intelligence Unit" — enter age, get analyst briefing with outlook (bullish/bearish/stable) and confidence rating

## Deployment

- **Repo:** https://github.com/jermainebethune/currency-by-age
- **Live site:** https://jermainebethune.github.io/currency-by-age/
- **Hosting:** GitHub Pages via Actions workflow (`.github/workflows/pages.yml`)
- **Branch:** `main` — push to main triggers automatic deployment

## Working on This Project

- When adding a new edition, create a new HTML file at root. Keep it self-contained (inline CSS/JS, no external deps besides Google Fonts).
- Follow the pattern: each edition must include all 7 currencies, an interactive section at the bottom, and responsive design.
- Update the README table and this file when adding new editions.
- All commits go to `main` — Pages deploys automatically on push.
- The interactive section at the bottom of each page lets users enter their age and get a personalized result. Each edition has ~16 age brackets with unique copy.

## Content Tone

Each edition matches its publication's editorial voice:
- **NYT:** Measured, literary, scroll-storytelling
- **WSJ:** Authoritative, data-driven, dry humor
- **New Yorker:** Wry, observational, literary, understated wit
- **Economist:** Global perspective, clever wordplay, treats whimsy with analytical seriousness
