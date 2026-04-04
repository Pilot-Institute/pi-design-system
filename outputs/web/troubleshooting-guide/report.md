# Processing Report — Troubleshooting Guide

**Input:** `troubleshooting-guide.html` (standalone, external file)
**Output:** `outputs/web/troubleshooting-guide/troubleshooting-guide.html`
**Segment:** Airplanes (default)
**Date:** 2026-04-03
**Spec version:** DESIGN.md (current), PI-Colour-Palette.csv (synced 2026-04-03)

---

## Changelog

### Fonts
| Before | After | Rule |
|--------|-------|------|
| `'Lexend'` via Google Fonts | `'Eina', Arial, system-ui…` (display) | DESIGN.md §5 — Eina for all headings/display |
| `'Lexend'` for body and UI | `Arial, system-ui…` (body) | DESIGN.md §5 — Arial for all body, UI, labels |
| `font-weight: 800` on hero h1 | `font-weight: 500` | Display Hero spec: weight 500 |
| `font-weight: 300` on hero p | `font-weight: 400` | Arial body: weight 400 |
| `font-weight: 300` on contact-banner p | `font-weight: 400` | Arial body: weight 400 |

**Note:** Eina is a licensed typeface. Until the `@font-face` declaration is added with the hosted font files, Arial renders as the approved fallback. The visual hierarchy is preserved.

---

### Off-palette colors corrected
All values below were absent from `PI-Colour-Palette.csv` and have been replaced with the nearest authoritative token.

| Element | Before | After | Token |
|---------|--------|-------|-------|
| `--pi-dark-blue` (text on light) | `#293A4E` | `#000000` | Black |
| Hero gradient mid-stop | `#1a2a4a` | `#0D0F20` | Midnight Navy |
| `tag.community` text | `#0b7ad8` | `#2398FF` | Sky Blue |
| `tag.course` text | `#293A4E` | `#000000` | Black |
| `.guide-body-inner` body text | `#4a5568` | `#000000` | Black |
| `.chevron` default color | `#b0b8c4` | `#82898D` | Ash Gray |
| `.footer` text | `#8896a6` | `#82898D` | Ash Gray |
| Contact banner gradient second stop | `#1a2a4a` | removed — solid Midnight Navy | Midnight Navy |

---

### Component updates

**Navigation / Header**
- Background changed to `rgba(13,15,32,0.95)` + `backdrop-filter: blur(12px)` per Dark Navigation spec
- Added `border-bottom: 1px solid #1D3B61` (Steel Blue) per spec
- Nav links updated: Arial 13px 700 uppercase, letter-spacing 0.04em
- Wordmark unchanged — "pilot" White / "institute" Sky Blue is already correct

**Hero section**
- Replaced 3-stop off-palette gradient with Midnight Navy solid + graph paper grid overlay (`rgba(35,152,255,0.08)` lines at 24px grid)
- This is the signature PI dark surface treatment (DESIGN.md §1, §10)
- Radial glow accents retained — colors are within-spec opacity variants of Sky Blue and Magenta Pink
- `letter-spacing` changed from `-0.03em` to `-0.5px` (Display Hero spec)
- `line-height` changed from `1.15` to `1.00` (Display Hero spec)
- Section vertical padding: `80px 48px 72px` → `96px 48px 80px` (spec: 96px desktop section spacing)

**Search input**
- `border-radius: 100px` (pill) → `6px` (Standard — spec inputs use 6px)
- Background: `rgba(255,255,255,0.07)` → `#080927` (Ink Blue — dark mode input spec)
- Border: `rgba(255,255,255,0.12)` → `1px solid #1D3B61` (Steel Blue — dark mode input spec)
- Focus: `box-shadow: 0 0 0 3px rgba(35,152,255,0.25)` per spec

**Quick-link cards**
- Border: `transparent` → `1px solid #B9CDCB` (Cool Gray — Light Card spec)
- Border-radius: `12px` → `8px` (Light Card spec)
- Hover transform: `translateY(-3px)` → `translateY(-2px)` (more restrained)
- Shadow scale updated to spec elevation levels

**Guide item cards (accordion)**
- Border: `rgba(0,0,0,0.04)` → `1px solid #B9CDCB` (Cool Gray — Light Card spec)
- Border-radius: `12px` → `8px` (Light Card spec)
- Shadow: updated to spec elevation scale (level 1 resting, level 2 hover/open)

**Warning callouts**
- Border and background color: Magenta Pink → **Orange `#FF6600`** (semantic warning/caution state per DESIGN.md §4)
- Magenta Pink is reserved for alerts and CTAs, not content-level warnings

**Contact banner**
- Replaced off-palette gradient (`var(--pi-navy)` → `#1a2a4a` → `var(--pi-dark-blue)`) with Midnight Navy + graph paper grid
- Consistent with the spec's dark surface treatment and the hero

**Contact button**
- `border-radius: 100px` (pill) → `6px` (Standard — primary button spec)
- Font: `'Lexend'` → Arial 13px 700 uppercase, letter-spacing 0.04em
- Hover: removed `translateY(-2px)` transform — not in spec; replaced with `box-shadow` glow
- Focus ring added: `2px solid #2398FF` with `outline-offset: 2px` per spec
- Active state added: Bright Blue + inset shadow per spec

**Tags**
- Overline scale applied: 11px (0.6875rem), letter-spacing 0.08em per spec
- `tag.course` color fixed: `#293A4E` → `#000000` (Black)
- `tag.community` color fixed: `#0b7ad8` → `#2398FF` (Sky Blue)

**Footer**
- Font size: `0.85rem` → `0.75rem` (12px — Caption scale per spec)

---

## Recommendations

### High priority

**1. Replace Eina fallback with actual font files**
Currently renders in Arial. Obtain the licensed Eina font files from the PI brand asset folder and add a `@font-face` declaration at the top of the CSS. The hierarchy (display hero, section headings, accordion titles) will immediately look more on-brand once the geometric sans-serif is in place.

**2. Replace text wordmark with SVG logo**
The current nav shows text ("pilotinstitute"). Replace with the official SVG horizontal lockup:
```html
<img src="[path]/PI_logo_hor-light.svg" alt="Pilot Institute" height="26">
```
Per DESIGN.md §3, the horizontal lockup (shield + wordmark) is the primary nav logo treatment.

**3. Search input: consider keeping a larger touch target**
The spec calls for `padding: 12px 16px` on inputs. The hero search bar currently uses `14px 20px` padding — this is intentional and appropriate for the hero context (larger visual weight). This is a justified deviation and can be documented as a hero-specific variant if the spec is extended to cover a search bar component.

---

### Medium priority

**4. Add mobile hamburger menu**
Per DESIGN.md §12, mobile navigation should collapse to a hamburger that opens a full-screen Midnight Navy overlay. Currently the nav links simply hide below 640px. The hamburger menu is not implemented.

**5. Quick-link icons: replace emoji with SVG icons**
The quick links use emoji (🔑, 🔒, 📝, etc.). These render differently across operating systems and don't conform to the PI icon system (flat, filled or 2px stroke, consistent geometric weight). Replace with SVGs from the system icon set using the Icon-LG size (32px) in Sky Blue or Magenta Pink on the tinted container.

**6. Hero search pill → sharp corners pattern consideration**
The current spec uses `6px` for all inputs. For future iterations, if a pill-shaped search bar is desired for the hero, this should be documented as a module-level exception in a `modules/web/help-center.md` file — not applied ad hoc.

**7. "Course Feature" tag color**
Currently `tag.course` renders in Black on a very low-opacity black background — low visual distinction. Consider defining a specific token for the Course tag: Steel Blue (`#1D3B61`) text on `rgba(29,59,97,0.10)` background, or Slate Blue (`#212353`) — both are in the CSV and would give the tag more character without violating spec.

---

### For the module spec (future)

When a `modules/web/help-center.md` (or similar) module is written, it should codify:
- Accordion component spec (border, radius, open/closed states, animation duration)
- Help tag taxonomy and colors (Common Issue, Course Feature, Account/Tech, Community)
- Callout variants (info / warning / tip) with the correct semantic color per type
- Search bar hero variant (input sizing within a dark hero context)
- Grid column behavior for quick-links at each breakpoint

---

## Token audit summary

| Category | Status |
|----------|--------|
| Colors | All corrected to CSV palette. Zero off-palette values remain in output. |
| Typography | Eina/Arial stack in place. Eina requires font files to render. |
| Spacing | Section padding updated to spec scale (96px desktop). |
| Elevation | Light mode shadow scale applied throughout. |
| Radius | All components use spec radius tokens. |
| Buttons | Primary button spec applied. Pill removed. |
| Navigation | Dark nav spec fully applied. |
| Segment | Airplanes (default). Sky Blue as primary. |
