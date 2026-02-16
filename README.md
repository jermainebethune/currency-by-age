# Principal Currencies by Age

An interactive illustrated essay exploring the idea that what people value most — their "currency" — changes at every stage of life. From blocks at age 1 to time at age 61, each version tells the same story through the lens of a different iconic publication's design language.

## Live Demo

**[View the project](https://jermainebethune.github.io/currency-by-age/)**

## The Four Editions

| Page | Style | Live Link |
|------|-------|-----------|
| `index.html` | **The New York Times** | [View](https://jermainebethune.github.io/currency-by-age/) |
| `wsj.html` | **The Wall Street Journal** | [View](https://jermainebethune.github.io/currency-by-age/wsj.html) |
| `newyorker.html` | **The New Yorker** | [View](https://jermainebethune.github.io/currency-by-age/newyorker.html) |
| `economist.html` | **The Economist** | [View](https://jermainebethune.github.io/currency-by-age/economist.html) |

## The Seven Currencies

| Age | Currency | The Idea |
|-----|----------|----------|
| 1 yr | Blocks | Before language, before money — stacking things is the entire economy |
| 5 yrs | Cookies | The first medium of exchange. Good behavior has a price |
| 16 yrs | Car Rides | Freedom is a set of car keys and whoever holds them has all the power |
| 25 yrs | Lattes | Every friendship, crisis, and career move starts with "let's grab coffee" |
| 31 yrs | Sleep | You would trade anything — anything — for eight uninterrupted hours |
| 45 yrs | Actual Money | After decades of abstraction, the literal currency finally takes center stage |
| 61 yrs | Time | The final currency. The one you can't earn back |

## Design Approaches

### New York Times
Scroll-driven longform storytelling. Playfair Display serif headlines, full-viewport sections, pull quotes with black left borders, chapter navigation dots, reading progress bar, and a dark interlude section. Minimal color — nearly all black and white.

### Wall Street Journal
Data-forward financial journalism. Stipple-dot SVG illustrations mimicking the iconic WSJ hedcut style, a scrolling stock ticker with currency symbols (BLKS, COOK, RIDE, LATT, SLEP, USD, TIME), "By the Numbers" sidebars, and an interactive portfolio builder with a donut chart.

### The New Yorker
Literary single-column magazine layout. Thin line-art cartoon illustrations with dry, understated captions. Drop caps, dinkus dividers, generous whitespace, and a narrow reading column. An interactive "Letters to the Editor" section generates personalized New Yorker-style cartoon captions.

### The Economist
Authoritative global analysis with punny headlines. Signature red top bar, canvas-rendered data visualizations for each currency (bar charts, line charts, area charts), a Global Currency Index ranking table, and an "Economist Intelligence Unit" interactive that delivers analyst briefings.

## Tech

Each page is a single self-contained HTML file. No build tools, no frameworks, no bundlers.

- HTML5 + CSS3 + vanilla JavaScript
- Google Fonts (loaded via CDN)
- SVG illustrations (inline)
- Canvas charts (The Economist edition)
- Intersection Observer API for scroll animations
- Fully responsive

## Inspiration

Based on [this illustration](https://github.com/jermainebethune/currency-by-age) of "Principal Currencies by Age" — the observation that what we trade for happiness shifts with every chapter of life.
