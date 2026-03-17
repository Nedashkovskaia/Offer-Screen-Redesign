# Uncapped — Funding Offer Screen Prototype

**Senior Product Designer case study — 2026**

A high-fidelity interactive prototype for Uncapped's funding offer screen.
Designed to reduce anxiety and build confidence at the highest-stakes moment in the funding journey.

---

## How to run

No build step. No server required.

```
Open offer-screen-prototype-v1.html in any modern browser.
```

---

## What this prototype covers

A founder (Brian) has been approved for up to **$100,000** in revenue-based funding.
This screen lets them understand the offer, choose an amount, and move forward — calmly.

### Sections

| Section | Purpose |
|---|---|
| **Approval header** | Acknowledge the emotional moment before presenting terms |
| **Offer cards** | Three pre-built scenarios to reduce decision paralysis |
| **Customize offer** | Slider + term + repayment date for founders who want control |
| **Offer summary** | Full cost transparency: amount, fee, total, first repayment date |
| **Repayment timeline** | Expandable SVG chart showing repayment progress over term |
| **Why Uncapped** | Product trust facts — no equity, no guarantee, one flat fee |
| **What is Next** | 3-step sequence that de-risks the CTA |
| **Sticky footer CTA** | Always-visible "Continue with Selected Offer" |
| **Contact overlay** | Support panel without navigating away |

---

## Offer cards

| Card | Amount | Weekly | Tag |
|---|---|---|---|
| Conservative | $60,000 | $2,654/wk | Low pressure |
| Balanced | $80,000 | $3,538/wk | Moderate |
| **Max capital** *(default)* | **$100,000** | **$4,423/wk** | ★ Recommended |

The right card (Max capital) is the recommended option and is pre-selected on load.

---

## Key interactions

- **Selecting a card** updates the entire summary block in real time
- **Customize tab** — amount slider ($50k–$100k), term (3/6/9/12 months), first repayment day (30/60/90)
- **Payment holiday fee** — appears in the summary only when day 60 (+2%) or day 90 (+3%) is selected
- **Repayment timeline** — expandable chart; x-axis starts at "Day 30" (or whichever day is selected)
- **Tooltip** on flat fee — hover the ⓘ icon for fee explanation

---

## Pricing model

```
Flat fee:     15% of capital
Holiday fee:  +2% (day 60) or +3% (day 90)
Total:        Capital + flat fee + holiday fee (if applicable)
Weekly:       Total ÷ (term months × 4.33 weeks)
Revenue %:    Weekly ÷ $65,000 (founder's weekly revenue)
```

No interest. No compounding. No early repayment penalties.

---

## Design system

Colours, typography, and components are based on the Uncapped Figma design library.

**Figma file:** `Senior Designer Case Study 2026 (Copy)`

Key colour tokens:

| Token | Value | Usage |
|---|---|---|
| `--green` | `#128081` | All interactive / CTA / accent |
| `--primary` | `#193a43` | Text and dark static UI only |
| `--green-light` | `#eaf6f6` | Selected / active backgrounds |
| `--text-secondary` | `#374d53` | Supporting text |
| `--text-tertiary` | `#879092` | Muted labels |

**Font:** Inter (prototype). Figma spec: Commissioner (headings) + Sora (body).

---

## Files

```
offer-screen-prototype-v1.html   Main prototype — all HTML, CSS, JS in one file
offer-screen-prototype-v1.md     Original content and UX specification
CLAUDE.md                        Instructions for AI-assisted development
README.md                        This file
```

---

## Scope notes — what v1 intentionally excludes

| Excluded | Reason |
|---|---|
| Real API / dynamic data | Prototype uses hardcoded values |
| Countdown timer | Avoids artificial urgency |
| Social proof / testimonials | Outside brief scope |
| Full repayment chart (default open) | Cognitive overload — available as expandable |
| Multiple term comparison view | Predefined cards handle this |

---

*Prototype v1 · Uncapped · Senior Product Designer case study 2026*
