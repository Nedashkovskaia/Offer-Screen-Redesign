# CLAUDE.md — Uncapped Offer Screen Prototype

This file tells Claude how to work with this codebase.

---

## Project overview

Single-file HTML prototype for Uncapped's funding offer screen.
File: `offer-screen-prototype-v1.html`
No build system. No dependencies. Open directly in a browser.

---

## File structure

Everything lives in one file in this order:

1. `<head>` — Google Fonts (Inter), all CSS in `<style>`
2. `<body>` — HTML markup
3. `<script>` — all JavaScript inline at the bottom

---

## Design tokens (CSS custom properties)

Defined in `:root`. Always use these — never hardcode colours.

```css
--bg              #FFFFFF          Page and card backgrounds
--surface         #f5f7f8          Structural surfaces (total row, etc.)
--primary         #193a43          Dark navy — text and dark UI only (NOT interactive)
--green           #128081          Brand teal — all interactive/CTA/accent
--green-hover     #00696b          Hover state for green elements
--green-light     #eaf6f6          Selected/active backgrounds
--green-mid       #c1e5e6          Hover borders
--text            #193a43          Primary body text
--text-secondary  #374d53          Secondary/supporting text
--text-tertiary   #879092          Muted, disabled, supporting labels
--border          #d7dee0          Default borders
--border-light    #e8edf0          Subtle borders
--radius          12px             Card corner radius
--radius-sm       8px              Button and small element radius
--content-width   800px            Max width of main content column
```

**Rule:** `--green` is for interactive elements. `--primary` is for static text/dark UI. Never swap them.

---

## Key CSS classes

### Layout
- `.content` — centred column, max-width `--content-width`
- `.section` — full-width section with padding, used for Why Uncapped and What is Next

### Cards
- `.offer-cards` — 3-column grid
- `.offer-card` — base card style; add `.selected` for active state
- `.offer-card--recommended` — right card (Max capital); has green border + shadow by default
- `.card-descriptor` — bold label at top of card (e.g. "Low pressure")
- `.card-tag` — uppercase category label (e.g. "CONSERVATIVE")

### Summary block
- `.summary-block` — container; no `overflow:hidden` (would clip tooltip)
- `.summary-row` — each row; `.total-row` for the highlighted total line
- `#sHolidayRow` — payment holiday fee row; hidden by default, shown via JS when holiday fee > 0

### Weekly summary
- `.weekly-main` — large weekly price
- `.weekly-sub` — single combined line: "Starts in 30 days · ~X% based on your revenue · N months"

### Tooltip
- `.tip-wrap` + `.tip-pop` — hover tooltip; requires parent `.summary-row` to have `position: relative`

---

## JavaScript state

All dynamic values live in one object:

```js
const S = {
    capital:        100000,   // selected funding amount
    termMonths:     6,        // repayment term
    repayDay:       30,       // first repayment day (30 / 60 / 90)
    holidayFeeRate: 0,        // 0 / 0.02 / 0.03
    baseFeeRate:    0.15,     // flat fee — always 15%
    weeklyRevenue:  65000,    // founder's weekly revenue (used for % calculation)
}
```

Always call `update()` after changing any value in `S`. `update()` recomputes all derived values and updates every DOM element.

### Key functions

| Function | Purpose |
|---|---|
| `update()` | Recomputes and renders all summary values |
| `selectCard(el)` | Sets `S.capital` + `S.termMonths` from clicked card |
| `syncCustomPanel()` | Syncs slider + term buttons to current `S` state |
| `onSlider()` | Handles amount slider input in Customize tab |
| `setTerm(months, btn)` | Sets repayment term |
| `setRepayDay(day, el)` | Sets first repayment day + holiday fee rate |
| `buildChart()` | Renders SVG repayment timeline chart |
| `toggleTimeline()` | Expands/collapses the chart panel |

### Card data

```js
const CARD_DATA = {
    conservative: { capital: 60000,  term: 6 },
    balanced:     { capital: 80000,  term: 6 },
    maximum:      { capital: 100000, term: 6 },  // default selected
}
```

Card `data-option` attribute must match a key in `CARD_DATA`.

---

## SVG chart

Built entirely by `buildChart()` using inline SVG.
Constants to know:

```js
const W     = 500    // viewBox width
const H     = 130    // viewBox height
const PAD_L = 4
const PAD_R = 12     // must be ≥ 10 to avoid clipping the endpoint circle (r=5)
const PAD_T = 36     // must be ≥ 36 to avoid "Fully repaid" text overlapping the line
const PAD_B = 8
```

X-axis first label reads `Day ${S.repayDay}` — updates when repayment day changes.

---

## Things to avoid

- Do not add `overflow: hidden` to `.summary-block` — it clips the tooltip
- Do not use `--primary` for interactive/CTA colours — use `--green`
- Do not hardcode colours in CSS or SVG — use tokens or the established hex values from the token list
- Do not reduce `PAD_R` below 10 in `buildChart()` — endpoint circle clips
- Do not reduce `PAD_T` below 36 in `buildChart()` — "Fully repaid" label overlaps the line

---

## Fonts

Currently: **Inter** (Google Fonts).
Figma spec: **Commissioner** (headings) + **Sora** (body) — not yet applied to prototype.
