# Uncapped — Offer Screen Prototype v1
## Ecommerce Founder Funding Offer

---

> **Prototype scope:** First iteration. Prioritises clarity, structure, and conversion
> over visual polish. Designed to reduce anxiety and build confidence at the
> highest-stakes moment in the funding journey.

---

## SECTION 1 — APPROVAL HEADER
*[Above the fold — primary]*
*[Purpose: Acknowledge the emotional moment before presenting terms]*

---

### Heading
**Your funding is approved, [First Name].**

### Subheading
Here's what you can access. Review your options and take it at your own pace.

### Expiry tag
*[Small, quiet label — not a banner, not bold, positioned top-right or below subheading]*

> This offer is reserved for you until **[Date: e.g. 24 March 2026]**.

*[Interaction note: Date is dynamically calculated as application date + 7 days.
Tone is reassuring, not pressuring. No countdown timer in v1.]*

---

---

## SECTION 2 — PREDEFINED OFFER OPTIONS
*[Above the fold — primary]*
*[Purpose: Reduce decision paralysis by presenting structured scenarios.
Founder chooses a starting point — customisation is optional, not required.]*

---

### Section label
**Choose a starting point**

*[Interaction note: Three cards displayed horizontally on desktop, stacked on mobile.
Middle card (Recommended) is pre-selected on load.
Selecting a card updates the offer summary in Section 3 in real time.]*

---

### Option 1 — Conservative
```
┌────────────────────────────────┐
│  £60,000 · 6 months            │
│                                │
│  £2,307 / week                 │
│  ~ 4% of your weekly revenue   │
│                                │
│  Lower weekly commitment.      │
│  Good if you want breathing    │
│  room while you grow.          │
└────────────────────────────────┘
```

---

### Option 2 — Recommended *(pre-selected)*
```
┌────────────────────────────────┐
│  ★ Recommended for [Business]  │
│                                │
│  £80,000 · 6 months            │
│                                │
│  £3,077 / week                 │
│  ~ 5% of your weekly revenue   │
│                                │
│  Sized to your revenue.        │
│  Most founders at your level   │
│  choose this option.           │
└────────────────────────────────┘
```

*[Interaction note: "Recommended for [Business Name]" uses connected store name
where available — e.g. "Recommended for Marble & Co." — makes the offer feel
specific and earned, not generic.]*

---

### Option 3 — Maximum
```
┌────────────────────────────────┐
│  £100,000 · 6 months           │
│                                │
│  £3,846 / week                 │
│  ~ 6% of your weekly revenue   │
│                                │
│  Full approved amount.         │
│  Higher weekly repayment.      │
│  Maximum capital available.    │
└────────────────────────────────┘
```

---

### Customisation link
*[Below the three cards — secondary, not prominent]*

> Want a different amount or term? **Customise your offer →**

*[Interaction note: Clicking expands a customisation panel below the cards —
amount slider, term selector (3 / 6 / 9 / 12 months), first repayment date
(Day 30 / 60 / 90). Panel is hidden by default. Does not replace the cards —
sits below them as an advanced option. All values in the offer summary update
in real time as the user adjusts.]*

---

---

## SECTION 3 — OFFER SUMMARY
*[Below the fold — primary]*
*[Purpose: Present cost with full transparency.
Structure follows: receive → repay → total cost.
Repayment is contextualised against the founder's actual revenue.]*

---

### Section label
**Your offer summary**

*[Interaction note: Values update dynamically when user selects a different
offer card in Section 2, or adjusts the customisation panel.]*

---

### Cost structure

| | |
|---|---|
| You receive | **£[Amount]** |
| Flat fee (15%) | **£[Fee]** ⓘ |
| Total to repay | **£[Total]** |

*[Tooltip on ⓘ: "This is the only fee you pay. No interest, no compounding,
no early repayment penalties. The full cost is shown here before you commit."]*

---

### Weekly repayment line

> **£[Weekly Amount] per week**
> Approximately **[X]% of your weekly revenue.**
> *Based on your connected [Shopify / WooCommerce / Amazon] store.*

*[Note: Revenue % is calculated from connected store data.
If data is unavailable, show a range: "approximately 5–7% of your weekly revenue
based on businesses similar to yours."]*

---

### Repayment schedule — expandable
*[Hidden by default — progressive disclosure]*

> **See full repayment schedule →**

*[Interaction note: Clicking expands a bar or step chart showing balance
declining week by week to zero. Chart is labelled with actual calendar dates,
not abstract "Month 1 / Month 2." Final bar is labelled "Fully repaid by
[Month Year]." Closing the chart does not reset any selections.]*

---

---

## SECTION 4 — WHY UNCAPPED
*[Below the fold — supporting]*
*[Purpose: Reinforce trust at the moment of maximum anxiety.
Specific product facts only — no brand marketing.]*

---

### Section label
**Why founders choose Uncapped**

---

### Trust points

> ✓ **No equity given up**
> Keep 100% ownership of your business. We never take a stake.

> ✓ **No personal guarantee required**
> Your business finances, not your personal assets.

> ✓ **One flat fee — nothing else**
> No interest. No compounding. No early repayment penalties.
> The full cost is shown above before you accept.

> ✓ **Repayments flex with your revenue**
> If sales slow, your weekly repayment slows too.
> No fixed monthly obligations that ignore how your business actually works.

> ✓ **Funds in your account within 24 hours of signing**
> Once your agreement is signed and KYC is complete.

---

---

## SECTION 5 — WHAT HAPPENS NEXT
*[Below the fold — supporting]*
*[Purpose: Remove the fear of irreversible commitment.
Founders need to know that accepting ≠ receiving funds immediately.
This section de-risks the CTA.]*

---

### Section label
**What happens after you accept**

---

### 3-step sequence

```
Step 1                    Step 2                    Step 3
──────────────────        ──────────────────        ──────────────────
Review your               Complete identity         Funds transferred
loan agreement            verification              within 24 hours

You'll receive a          A quick KYC check —       Once your agreement
full agreement to         usually takes under       is signed and KYC
read before               10 minutes.               is complete, capital
anything is                                         lands in your
finalised.                                          account.
```

---

---

## STICKY FOOTER — CTA AREA
*[Always visible — fixed to bottom of viewport on scroll]*
*[Purpose: Keep the commitment action reachable at all times
without interrupting the reading experience.]*

---

### Layout

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│   [  Secure this offer →  ]     [  Save and come back  ]    │
│                                                              │
│   Accepting now doesn't release funds —                      │
│   you'll review your full agreement first.                   │
│                                                              │
│                    Questions? Talk to a specialist →         │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

### Primary CTA
**Secure this offer →**

*[Interaction note: On click — show a brief confirmation state:
"Great. Let's get your agreement ready." → transition to agreement review step.
Do not use "Accept" or "Submit" — these imply finality.]*

---

### Secondary CTA
**Save and come back later**

*[Interaction note: Saves current selection (offer amount, term, repayment date).
Sends a follow-up email with offer summary and a direct link back to this screen.
Does not abandon the session — keeps the founder in the funnel.]*

---

### Reassurance line
> Accepting now doesn't release funds — you'll review your full agreement first.

*[Always visible in footer. This single line may be the most important
conversion copy on the entire screen.]*

---

### Support link
> Questions? **Talk to a specialist →**

*[Interaction note: On click — opens a compact panel (not a new page) with:]*

```
┌──────────────────────────────────┐
│  We're here if you need us.      │
│                                  │
│  [Book a 15-min call]            │
│  [Send us a message]             │
│  hello@uncapped.com              │
│                                  │
│  ✕ Close                         │
└──────────────────────────────────┘
```

*[Panel overlays the screen without navigating away.
Booking a call or sending a message does not lose the founder's offer selection.]*

---

---

## INTERACTION NOTES — FULL SUMMARY

| Element | Behaviour |
|---|---|
| Offer cards | Selecting a card updates Section 3 summary in real time |
| Recommended card | Pre-selected on page load |
| "Customise" link | Expands panel below cards — hidden by default |
| Customisation sliders | Update summary in real time |
| Fee tooltip | Opens inline — does not navigate away |
| Repayment schedule | Expands inline — progressive disclosure |
| Primary CTA | Transitions to agreement review — does not release funds |
| Secondary CTA | Saves selection + sends email with offer link |
| Support link | Opens contact panel overlay — does not navigate away |
| Expiry date | Dynamically set to application date + 7 days |
| Revenue % | Calculated from connected store data |
| Business name | Pulled from connected store where available |

---

---

## DYNAMIC VALUES — PLACEHOLDER REFERENCE

| Placeholder | Source |
|---|---|
| [First Name] | User account data |
| [Business Name] | Connected store name |
| [Date] | Application date + 7 days |
| [Amount] | Selected offer card / customisation slider |
| [Fee] | Amount × 15% |
| [Total] | Amount + Fee |
| [Weekly Amount] | Total ÷ (Term in weeks) |
| [X]% revenue | Weekly Amount ÷ Average weekly revenue from store |
| [Store type] | Shopify / WooCommerce / Amazon — from connected integration |
| [Month Year] | Start date + Term length |

---

---

## WHAT THIS PROTOTYPE DOES NOT INCLUDE (v1 scope)

The following are intentionally excluded from v1 to reduce complexity.
Each is a candidate for v2 based on validation findings.

| Excluded | Reason | v2 consideration |
|---|---|---|
| AI chat assistant | Risk of distracting from CTA | Add after core clarity is validated |
| Partner / platform logos | Feels like marketing at commitment stage | Replace with contextual store reference |
| Full repayment chart (default on) | Cognitive overload | Available as expandable — see Section 3 |
| Multiple term comparison | Too much configuration upfront | Predefined cards handle this |
| Testimonials / social proof | Not included in brief scope | Strong v2 addition |

---

*Prototype v1 — Uncapped Offer Screen Redesign*
*Case study: Senior Product Designer take-home task*
