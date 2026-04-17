# Module: Graphics — Editorial — Webinar Slides

> **Status: Active** — Authored from reference deck `Jan26 Pilot Institute Client Webinar.pptx` (42 slides). Apply these specs for all PI live webinar and recorded-webinar presentations built in PowerPoint or Google Slides.

---

## What this module covers

Branded slide decks used for PI live webinars, client webinars, and recorded-webinar presentations. These are high-conversion, sales-oriented decks with an educational core — not internal decks. The design language is dark-first, command-environment: deep navy canvas, electric blue highlights, bold display type, and tight click-reveal pacing.

---

## Canvas & Format

| Property | Value |
|---|---|
| Dimensions | 10 × 5.625 in (25.4 × 14.3 cm) |
| Aspect ratio | 16:9 widescreen |
| PowerPoint equivalent | 9,144,000 × 5,143,500 EMU |
| Google Slides equivalent | 1920 × 1080 px at presentation resolution |
| Orientation | Landscape only |

---

## Color Tokens

All colors must trace to `reference/PI-Colour-Palette.csv`. The table below lists the semantic role, the PI token name, and the hex used in webinar decks.

| Role | PI Token | Hex | Usage |
|---|---|---|---|
| Slide background | Midnight Navy | `#0D0F20` | All slides — solid fill, no gradient |
| Primary brand signal | Sky Blue | `#2398FF` | Left accent bar, numbered badges, stat card headers, CTA elements, two-color headline words |
| Light blue highlight | Baby Blue *(secondary)* | `#81D1F4` | Super-title labels, in-line text emphasis, stat descriptors, urgency callouts |
| Primary text | White | `#FFFFFF` | Main headings, body copy where full contrast needed |
| Near-white body | Light Gray | `#F0F0F0` | Default body and heading text on navy background |
| Dark panel / callout box | Deep Navy *(secondary)* | `#212353` | Inset callout boxes, quote panels, stat descriptor boxes, bonus strips |
| Gold / urgency accent | Amber Gold *(secondary)* | `#FFBE33` | CTA pill labels, limited use for pricing callouts |
| Magenta strike accent | Magenta Pink | `#F80590` | Strikethrough connector lines on pricing slides only |
| Subdued body | Steel Blue-Gray *(secondary)* | `#94A3B8` | Fine print, footnotes, legal copy |

> **Rule:** Do not use gradients on webinar slides. All fills are solid. Sky Blue `#2398FF` and Deep Navy `#212353` are the only shape fill colors used at scale.

---

## Typography

| Role | Font | Weight | Size range | Color |
|---|---|---|---|---|
| Display headline (title slides) | Arial Black | 900 | 48 pt – 72 pt | `#F0F0F0` or `#FFFFFF` |
| Section headline | Arial Black | 900 | 32 pt – 44 pt | `#F0F0F0` |
| Stat / callout figure | Arial Black | 900 | 48 pt – 60 pt | `#F0F0F0` or `#2398FF` |
| Super-title label | Arial | Regular | 13 pt – 15 pt | `#81D1F4` |
| Body copy | Arial | Regular | 15 pt – 18 pt | `#F0F0F0` or `#FFFFFF` |
| Badge / pill label | Arial | Bold | 10 pt – 13 pt | `#FFFFFF` |
| Fine print | Arial | Regular | 10 pt – 12 pt | `#94A3B8` |
| CTA price display | Arial Black | 900 | 96 pt – 144 pt | `#2398FF` |

**Two-color headline rule:** Key words or short phrases within a headline are set in `#2398FF` (Sky Blue) or `#81D1F4` (Baby Blue) while the rest of the line remains `#F0F0F0`. This is the primary in-line emphasis device — do not use italic or underline.

**Eina note:** Eina is the primary brand typeface, but webinar decks are built in PowerPoint/Google Slides where Eina is not reliably available. Arial Black substitutes for Eina 03 SemiBold/Bold in all slide contexts. If a future production pipeline embeds fonts, Eina 03 SemiBold should replace Arial Black at equivalent weights.

---

## Slide Layout Types

### 1. Hero / Title Slide

The opening slide. Sets the event context and earns attention in the first 3 seconds.

**Structure:**
- Full-bleed background image (aviation photography or dark atmospheric visual) at 100% canvas coverage, positioned behind all elements
- PI logo — horizontal lockup, light variant — top-left or top-center
- Urgency CTA bar — top-right corner, `#2398FF` fill, white bold text (~13 pt), e.g. "FREE PDF BONUS — Stay to the end!"
- Main headline — Arial Black, 60–72 pt, two-color treatment: primary claim in `#F0F0F0`, key hook word/phrase in `#2398FF`
- Subtitle — Arial, 18 pt, `#2398FF`, one line
- Optional "presents" label above logo, white, 18 pt

**Background image treatment:** Image is the base layer at z-order 0. A semi-transparent dark overlay may be applied if the image risks reducing text legibility — test at 100% brightness before adding overlay.

---

### 2. Agenda / Promise Slide

"By The End of This Webinar…" — sets expectations and builds commitment.

**Structure:**
- Background: Midnight Navy solid, no image
- Left accent bar (see Component: Left Accent Bar)
- Section headline: Arial Black, 36 pt, `#F0F0F0`
- 3–5 numbered bullet points, each consisting of:
  - Numbered circle badge (see Component: Numbered Badge) — `#2398FF` fill, white number
  - Body text: Arial, 15–18 pt, `#F0F0F0`
  - Key data point or hook phrase within the line set in `#81D1F4`
- Each bullet group is click-animated (entrance animation, no auto-advance)

---

### 3. Pre-Show / Holding Slide

Used before the webinar starts. Emotionally engaging — addresses the attendee's doubt or aspiration.

**Structure:**
- Background: Midnight Navy solid
- Left accent bar
- Super-title: Arial, 15 pt, `#81D1F4`, above the main heading
- Main heading: Arial Black, 36 pt, `#F0F0F0`
- Body text: Arial, 15 pt, `#F0F0F0`, intro sentence
- 2–3 quote panels (see Component: Dark Callout Box) — each containing a single quote line in `#81D1F4`
- Footer line: Arial, 15 pt, `#F0F0F0` with key phrase in `#81D1F4`
- Quote panels are click-animated (reveal one at a time)

---

### 4. Content / Argument-Build Slide

The workhorse slide type. Used for problem agitation, insight delivery, and framework explanation.

**Structure:**
- Background: Midnight Navy solid
- Left accent bar
- Super-title: Arial, 15 pt, `#81D1F4` — short framing label (e.g. "But Here's the Thing…")
- Main headline: Arial Black, 44–60 pt, `#F0F0F0`, two-color treatment
- Supporting points: Arial, 18 pt, `#F0F0F0`, 2–4 lines, each click-animated
- Closing statement: Arial, 18 pt, `#FFFFFF`, bottom of slide — often uses a Dark Callout Box for the punchline
- Optional: one Dark Callout Box (`#212353`) containing the key takeaway or rhetorical statement

**Density rule:** Maximum 4 click-animated reveals per content slide. If more points are needed, split into two slides.

---

### 5. Section Divider / "Secret" Slide

Signals a major section transition. Uses the "Secret #X" pill badge.

**Structure:**
- Background: Midnight Navy solid
- Left accent bar
- Secret badge pill (see Component: Secret Badge Pill) — top-left content area
- Context label: Arial, 15 pt, `#81D1F4` — the false belief or challenge being addressed
- Section title: Arial Black, 36–44 pt, `#F0F0F0`
- Optional sub-copy: Arial, 15–18 pt, `#F0F0F0`

---

### 6. Statistics / Data Slide

High-impact data delivery. Uses the Stat Card Module component.

**Structure:**
- Background: Midnight Navy solid
- Left accent bar
- Secret badge pill (when inside a secrets framework)
- Context label: Arial, 15 pt, `#81D1F4`
- Section title: Arial Black, 36–44 pt, `#F0F0F0`
- 2–4 Stat Card Modules in a horizontal row (see Component: Stat Card Module)
- Each stat card is click-animated
- Closing line: Arial, 18 pt, `#FFFFFF`, full width below stat cards

---

### 7. Framework / Numbered Pillars Slide

Introduces a multi-step framework or system. Numbered, structured, aspirational.

**Structure:**
- Background: Midnight Navy solid
- Left accent bar
- Section title: Arial Black, 36 pt, `#F0F0F0`, with drop shadow (`outerShdw`, 4 pt, 45° angle, 50% alpha black)
- Subtitle: Arial, 15 pt, `#FFFFFF`
- 3 numbered pillars in a horizontal row, each containing:
  - Numbered circle badge (large, `#2398FF` fill)
  - Pillar title: Arial Black, 20–24 pt, `#F0F0F0`
  - Pillar description: Arial, 13–15 pt, `#F0F0F0`
- Bonus strip: Dark Callout Box (`#212353`) full-width, containing "+" bonus label in `#81D1F4`
- Closer text: Arial, 15–18 pt, `#FFFFFF`, 1–2 lines

---

### 8. Offer / Closing CTA Slide

The conversion slide. Often hidden and manually revealed by the presenter. Maximum visual urgency.

**Structure:**
- Background: Midnight Navy solid
- Hook line: Arial, 18 pt, `#FFFFFF` — acknowledges the attendee being present
- Offer headline: Arial Black, 36 pt, `#FFFFFF` — names the special offer (e.g. "48-Hour Webinar Special")
- Price display: Arial Black, 96–144 pt, `#2398FF` — the offer price dominates the slide
- Pricing context row: Arial Black, 24–28 pt — original price / savings amount / monthly breakdown, with monthly figure in `#81D1F4`
- Value anchors: Arial, 13–15 pt, `#F0F0F0` — 1–2 comparison lines below the price
- Urgency strip: full-width bar or text line, `#81D1F4`, "This offer expires in [X] hours"
- Optional: Magenta Pink (`#F80590`) connector line striking through the old price
- Optional: Dark Callout Box oval badge overlaying the urgency message
- Slide attribute: set `show="0"` in PowerPoint to hide until manually revealed

---

## Components

### Left Accent Bar

A vertical `#2398FF` (Sky Blue) filled rectangle pinned to the left edge of the slide, spanning full slide height. Width: approximately 0.9–1.1 inches (82,000–100,000 EMU). Used on all content slides except the Hero/Title slide and the Offer slide.

**Purpose:** Provides consistent left-edge brand signal across the deck. Anchors the visual frame.

---

### Numbered Badge

A solid `#2398FF` filled circle (approximately 0.45 in diameter) containing a bold white number in Arial Black. Used for agenda bullets, pillar items, and any ordered list requiring visual separation.

**Size:** 40,000–45,000 EMU diameter. Center number text vertically and horizontally. Number: Arial Black, 16–20 pt, `#FFFFFF`.

---

### Secret Badge Pill

A rounded rectangle (`#2398FF` fill, corner radius ~8 pt) labeled "SECRET #[N]" in white Arial Bold, 11–13 pt. Positioned in the top-left content area (below the left accent bar zone). Used to signal the N-th secret in the webinar framework.

---

### Dark Callout Box

A solid `#212353` (Deep Navy) filled rectangle with no border. Used to create visual separation for pull-quotes, key statements, bonus items, or rhetorical closers. Content inside uses `#81D1F4` (Baby Blue) for emphasis text and `#FFFFFF` for body text.

**Do not** use `#0D0F20` (Midnight Navy) for these boxes — the contrast between `#212353` and the `#0D0F20` background must be visible.

---

### Stat Card Module

A two-part stacked card used for data slides:

- **Top cell:** `#2398FF` (Sky Blue) filled rectangle, containing the large statistic figure in Arial Black, 48–60 pt, `#FFFFFF` or `#F0F0F0`
- **Bottom cell:** `#212353` (Deep Navy) filled rectangle directly beneath, same width, containing the label in Arial, 13–15 pt, `#F0F0F0`

Multiple stat cards are arranged in a horizontal row with equal spacing. Each card is click-animated to appear individually.

---

## Animation Rules

| Rule | Detail |
|---|---|
| Trigger | All content reveals use click-triggered entrance animations |
| Auto-advance | Never — every reveal requires a presenter click |
| Preset class | `entr` (entrance) — fade or appear, no motion paths |
| Order | Top-to-bottom, left-to-right within each slide |
| Stat cards | Each card group animates as a single unit per click |
| Offer slide | Entire slide is hidden (`show="0"`); the reveal is manual via slideshow controls, not animation |

---

## Logo Placement

| Slide type | Logo position | Logo variant |
|---|---|---|
| Hero / Title | Top-left or top-center | Light (white wordmark) |
| Content slides | Not repeated per slide — logo appears on title and closing slides only |
| Offer / Closing | Optional — bottom-right if used | Light |

Do not place the PI logo on every slide. Its value is in the opening and closing frames.

---

## Segment Overrides

Apply the segment primary color in place of Sky Blue `#2398FF` for:
- Left accent bar fill
- Numbered badge fills
- Stat card header fills
- Secret badge pill fills
- Two-color headline words

All other tokens (background, text, callout box, urgency) remain unchanged.

| Segment | Primary Color Token | Hex |
|---|---|---|
| Airplanes (default) | Sky Blue | `#2398FF` |
| Drones | *(see `segments/drones.md`)* | — |
| Helicopters | *(see `segments/helicopters.md`)* | — |
| Flight Attendant | *(see `segments/flight-attendant.md`)* | — |

---

## Slide Structure Checklist

Before finalizing any webinar deck:

- [ ] All backgrounds are Midnight Navy solid — no gradients, no other fill colors
- [ ] Left accent bar present on all content slides (not on hero or offer slide)
- [ ] Every headline uses the two-color treatment (primary word/phrase in Sky Blue or Baby Blue)
- [ ] All fonts are Arial Black (display) or Arial (body) — no other typefaces
- [ ] All colors trace to a row in `PI-Colour-Palette.csv`
- [ ] Logo appears on title slide only (and optionally on closing/offer slide)
- [ ] All content reveals are click-triggered — no auto-advance
- [ ] Offer slide is hidden (`show="0"`) unless the deck is a static reference version
- [ ] No decorative elements (gradients, shadows, patterns) except the drop shadow on Framework slide titles

---

## Known Owners

- Graphic Designer: Zhenia
- Reference file: `reference/img/Jan26 Pilot Institute Client Webinar.pptx`
