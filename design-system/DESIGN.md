# Design System: Pilot Institute

## 1. Visual Theme & Atmosphere

Pilot Institute's design surface is a flight operations room after dark — midnight navy walls textured with the grid of an aviation sectional chart, instruments glowing in electric blue and hot magenta. This is not a neutral canvas; it is a command environment. Every element exists with purpose, every color carries signal value. The experience communicates that learning to fly is a serious undertaking made genuinely accessible — authoritative enough to trust your certificate to, clear enough for a first-time student to navigate without a guide.

The signature design move is the graph paper grid: fine blue lines on deep navy that evoke the charts, logbooks, and instrument panels that define aviation's visual language. Against this structured ground, content floats with precision — headlines in Eina's geometric sans-serif land like cockpit callouts, Sky Blue links and buttons read as active displays, and Magenta Pink alerts fire like warning indicators. Nothing decorates for its own sake.

What makes Pilot Institute's design language unmistakable is its dual-mode identity. The dark mode is primary — a command environment built for focus and energy. The light editorial mode (white backgrounds, Sky Blue section headers, Arial body text) appears in study sheets, white papers, and reference documents, where printability and sustained reading take precedence over visual drama. The brand moves between these modes fluently, holding identity through consistent color, typography, and logo treatment.

**Key Characteristics:**
- Midnight Navy (`#0D0F20`) canvas with graph paper grid overlay — the signature surface
- Sky Blue (`#2398FF`) and Magenta Pink (`#F80590`) as the two primary brand signals
- Dark-first design philosophy: navy is home, white is document mode
- Eina geometric sans-serif for all display and heading type — precise, confident, approachable
- Gobold condensed display for maximum-impact moments only — used like a klaxon, never casually
- Arial for all body, UI, and functional text — unambiguous, universally available
- Sky Blue → Magenta Pink linear gradients on hero imagery and course cards
- Flat vector illustration style in brand colors — simplified aviation characters and icons
- High-contrast pairing: White text on navy; Sky Blue and Pink as the only chromatic elements
- Clean two-column white layout for print and editorial materials

---

## 2. Color Palette & Roles

All colors are sourced exclusively from `PI-Colour-Palette.csv`. Every hex value below is authoritative from that file.

### Primary Surfaces (Dark Mode)
- **Midnight Navy** (`#0D0F20`): The primary dark page background and signature design surface. All dark-mode layouts begin here. Carries the graph paper grid overlay. The most-used dark surface in the system.
- **Navy Blue** (`#000033`): The deepest dark background — used beneath full-bleed hero sections and as the base layer for the highest-drama moments.
- **Ink Blue** (`#080927`): Dark card and container background placed on Midnight Navy surfaces. Creates the first level of surface layering.
- **Slate Blue** (`#212353`): Elevated card and prominent container surface. Noticeably lighter than Ink Blue, creating clear hierarchy.
- **Steel Blue** (`#1D3B61`): Borders, dividers, and surface edges in dark sections. The visible boundary between surfaces.
- **Deep Violet** (`#260545`): Rich dark surface for high-contrast nested containers and spotlight moments.
- **Dark Burgundy** (`#23061C`): Deep warm-toned dark surface — used for cards that need warmth rather than blue coolness.
- **Deep Plum** (`#3B1636`): Dark elevated surface overlay with purple warmth.
- **Rich Purple** (`#3A0256`): Dark accent surface for purple-family section variants.
- **Ink Blue (deep)** (`#080927`): see Ink Blue above.
- **Deep Teal** (`#000F17`): The absolute darkest surface — used only for the most immersive full-bleed dark environments.
- **Electric Indigo** (`#2E4292`): Mid-dark surface, background for interactive chart elements and feature grids.

### Primary Interactive
- **Sky Blue** (`#2398FF`): The primary brand blue — primary CTAs, active links, interactive highlights, icon backgrounds, table headers in light mode, and the origin point of the brand gradient. The single most-used chromatic color.
- **Bright Blue** (`#1877F2`): Hover and pressed state for Sky Blue interactive elements. Slightly deeper for visible feedback.
- **Magenta Pink** (`#F80590`): The signature brand accent — secondary CTAs, alert indicators, gradient terminus, callout backgrounds. Used with precision; never as a fill for large content areas.

### Light Surfaces (Editorial / Print Mode)
- **White** (`#FFFFFF`): Primary light page background — study sheets, white papers, the light preview mode.
- **Light Gray** (`#F0F0F0`): Alternate light background, card surface on white layouts.
- **Ivory** (`#FFF5E5`): Warm light card surface.
- **Linen** (`#F3ECD9`): Warm neutral callout area background in print layouts.
- **Cream** (`#FFF0D0`): Warmest light tint, used rarely in digital contexts.

### Text
- **White** (`#FFFFFF`): Primary text on all dark surfaces.
- **Black** (`#000000`): Primary text on all light surfaces.
- **Ash Gray** (`#82898D`): Secondary and caption text on light surfaces.
- **Cool Gray** (`#B9CDCB`): Tertiary text, metadata, and de-emphasised labels on light surfaces. Also used as border color on light layouts.

### Semantic States
- **Forest Green** (`#16A600`): Correct answer, pass state, success — the primary right/correct indicator in FAA and quiz content.
- **Lime Green** (`#63DB00`): Secondary success, strong completion badge.
- **Seafoam Green** (`#2AEAA7`): Soft success surface tint, progress completion.
- **Mint** (`#AFEAD6`): Lightest success surface for background tinting.
- **Tomato Red** (`#FF464A`): Error state, incorrect indicator, wrong signifier — the primary fail/wrong indicator.
- **Crimson** (`#E4262D`): Hard failure, danger state.
- **Brick Red** (`#82312C`): Deep error surface for error container backgrounds.
- **Chestnut** (`#5C231F`): Deepest error tone, high-severity warning surfaces.
- **Orange** (`#FF6600`): Warning state, caution indicator.
- **Amber** (`#F2A135`): Pending or attention-required state.
- **Orange Peel** (`#F96E11`): Notification badge, warm alert.
- **Tangerine** (`#F96611`): Warm alert accent, secondary notification.
- **Golden Yellow** (`#FFBE33`): Callout highlight, data emphasis, notification badge on dark.

### Illustration & Chart Accents
- **Lavender Purple** (`#8759F2`): Secondary illustration accent, chart series 2.
- **Aqua Blue** (`#0EBFE5`): Tertiary accent for data visualisation and infographics, chart series 3.
- **Cyan Sky** (`#5AD7ED`): Illustration highlight, chart series 4.
- **Turquoise** (`#3EBBD4`): Map and geography visualisations.
- **Ocean Blue** (`#029DCD`): Informational chart fills.
- **Baby Blue** (`#81D1F4`): Icon background tint, light blue chip.
- **Cerulean** (`#33A7F2`): Link hover on light surfaces.
- **Fuchsia** (`#E42A84`): Deep pink, gradient midpoint between Sky Blue and Magenta Pink variants.
- **Deep Magenta** (`#B9006E`): Deep pink accent for high-contrast moments.
- **Royal Purple** (`#7F1C7D`): Illustration accent, chart series color.
- **Lavender Mist** (`#E4DCF8`): Light badge background and callout surface on white layouts.
- **Coral** (`#ED683D`): Warmer warning variant.
- **Peach** (`#F6BC86`): Illustration warm tint, skin tones in character illustrations.
- **Blush** (`#F5ACA5`): Light pink illustration tint.
- **Brown** (`#663300`): Warm earth illustration accent.

### Gradient System
The PI gradient runs **Sky Blue** (`#2398FF`) → **Magenta Pink** (`#F80590`) at 135°. It represents the brand's arc from technical clarity to energetic action. Applied to: course card overlays, hero section accents, and gradient CTA buttons. A secondary gradient Sky Blue → **Lavender Purple** (`#8759F2`) is used for calmer informational contexts. Neither gradient is applied to text or UI labels.

---

## 3. Typography Rules

### Font Families
- **Display / Headline**: `Eina`, fallback: `Arial, system-ui, -apple-system, 'Helvetica Neue', sans-serif`
- **Impact**: `Gobold`, fallback: `'Arial Black', Impact, sans-serif`
- **Body / UI**: `Arial`, fallback: `system-ui, -apple-system, 'Helvetica Neue', sans-serif`

*Eina is a licensed geometric sans-serif with Regular, SemiBold, Bold, and Italic variants. When unavailable, use Arial — do not substitute Montserrat, Futura, or other geometric fonts, as they alter the brand's proportions. Gobold is a condensed bold display font used exclusively in all-caps at large display sizes.*

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Usage |
|------|------|------|--------|-------------|----------------|-------|
| Gobold Impact | Gobold | 80–120px (5–7.5rem) | 700 | 0.92 | -1px | Full-bleed dark section callouts, video text overlays. All-caps only. |
| Display Hero | Eina | 64px (4rem) | 500 | 1.00 | -0.5px | Primary hero headline |
| H1 | Eina | 52px (3.25rem) | 400 | 1.05 | -0.3px | Page-level headings |
| H2 | Eina | 40px (2.5rem) | 500 | 1.10 | -0.2px | Section headings |
| H3 | Eina | 32px (2rem) | 500 | 1.15 | normal | Sub-section headings, card titles |
| H4 | Eina | 24px (1.5rem) | 500 | 1.20 | normal | Component headings |
| H5 | Eina | 20px (1.25rem) | 500 | 1.25 | normal | Small section headings, list labels |
| Body Large | Arial | 18px (1.125rem) | 400 | 1.65 | normal | Intro paragraphs, lead text |
| Body | Arial | 16px (1rem) | 400 | 1.60 | normal | Standard body copy, UI text |
| Body Small | Arial | 14px (0.875rem) | 400 | 1.55 | normal | Secondary body, footnotes |
| Label / Button | Arial | 13px (0.8125rem) | 700 | 1.40 | 0.04em | Button text, nav links, form labels — always uppercase |
| Table Header | Arial | 13px (0.8125rem) | 700 | 1.40 | 0.02em | Table column headers |
| Caption | Arial | 12px (0.75rem) | 400 | 1.45 | normal | Metadata, image credits, timestamps |
| Overline | Arial | 11px (0.6875rem) | 700 | 1.40 | 0.08em | Category labels, section eyebrows — always uppercase |
| Micro | Arial | 10px (0.625rem) | 400 | 1.40 | normal | Legal text, footnote subscripts |
| Table Body | Arial | 14px (0.875rem) | 400 | 1.55 | normal | Table data cells |

### Typographic Philosophy
- **Eina for authority, Arial for utility**: Eina headings carry the brand's precision and confidence; Arial handles every functional communication task with absolute clarity.
- **Gobold as a klaxon**: Gobold appears only at 80px or larger, always all-caps, always on dark backgrounds. It is a P.A. announcement — commanding and brief. Never use it for sub-headlines, labels, or anything below 60px.
- **Tight headlines, generous body**: Display type uses line-heights of 0.92–1.20 for billboard impact. Body text opens to 1.60–1.65 for sustained readability. This range alone creates legible visual hierarchy.
- **Weight discipline**: Eina headings use 400–500 for light surfaces and 300–400 for dark surfaces — the slightly heavier weight on white backgrounds compensates for reduced contrast. Gobold at 700 handles all maximum-impact moments. Arial body text uses 400 for copy and 700 for labels, buttons, and table headers.
- **Labels and overlines are always uppercase**: Any text 13px or below serving as a category marker, button label, or eyebrow uses uppercase with letter-spacing 0.04–0.08em.

---

## 4. Component Stylings

### Buttons

**Primary — Sky Blue**
- Background: Sky Blue (`#2398FF`)
- Text: White (`#FFFFFF`), Arial 13px weight 700, uppercase, letter-spacing 0.04em
- Padding: 12px 24px
- Radius: 6px
- Hover: Bright Blue (`#1877F2`) background, transition 0.2s ease
- Focus: 2px solid offset ring in Sky Blue (`#2398FF`), outline-offset 2px
- Active: Bright Blue + `inset 0 2px 4px rgba(0,0,0,0.30)`
- Transition: background-color 0.2s ease, box-shadow 0.2s ease

**Secondary — Magenta Pink**
- Background: Magenta Pink (`#F80590`)
- Text: White (`#FFFFFF`), Arial 13px weight 700, uppercase
- Padding: 12px 24px
- Radius: 6px
- Hover: Fuchsia (`#E42A84`) background, transition 0.2s ease
- Focus: 2px offset ring in Magenta Pink
- Active: Fuchsia + `inset 0 2px 4px rgba(0,0,0,0.30)`

**Gradient CTA**
- Background: `linear-gradient(135deg, #2398FF, #F80590)`
- Text: White (`#FFFFFF`), Arial 13px weight 700, uppercase
- Padding: 12px 28px
- Radius: 6px
- Hover: opacity 0.88, scale(1.02), transition 0.2s ease
- Focus: 2px offset ring in Sky Blue
- Active: scale(0.98), opacity 0.84

**Outline — on dark surfaces**
- Background: transparent
- Border: 1.5px solid Sky Blue (`#2398FF`)
- Text: Sky Blue (`#2398FF`), Arial 13px weight 700, uppercase
- Padding: 11px 23px
- Radius: 6px
- Hover: `rgba(35,152,255,0.12)` background fill, transition 0.2s ease
- Focus: 2px offset ring in Sky Blue
- Active: `rgba(35,152,255,0.22)` background

**Ghost — on light surfaces**
- Background: transparent
- Border: 1.5px solid Black (`#000000`)
- Text: Black (`#000000`), Arial 13px weight 700, uppercase
- Padding: 11px 23px
- Radius: 6px
- Hover: Light Gray (`#F0F0F0`) background, transition 0.2s ease
- Focus: 2px offset ring in Slate Blue (`#212353`)

### Cards

**Dark Card (default)**
- Background: Ink Blue (`#080927`)
- Border: 1px solid Steel Blue (`#1D3B61`)
- Radius: 12px
- Padding: 24px
- Shadow: `0 4px 16px rgba(0,0,0,0.40)`
- Hover: border-color → Sky Blue (`#2398FF`), shadow → `0 8px 24px rgba(0,0,0,0.50)`, transition 0.2s ease
- Focus (keyboard): 2px offset ring in Sky Blue

**Course Card (photography + gradient overlay)**
- Background: photography with `linear-gradient(to bottom, transparent 30%, #0D0F20 100%)`
- Top accent: 3px border in `linear-gradient(135deg, #2398FF, #F80590)`
- Radius: 12px
- Padding: 20px (bottom-anchored text)
- Hover: scale(1.02), shadow lifts, transition 0.25s ease

**Light Card (editorial / print)**
- Background: White (`#FFFFFF`)
- Border: 1px solid Cool Gray (`#B9CDCB`)
- Radius: 8px
- Padding: 24px
- Shadow: `0 2px 8px rgba(0,0,0,0.08)`
- Hover: border → Sky Blue (`#2398FF`), shadow → `0 4px 16px rgba(0,0,0,0.12)`, transition 0.2s ease

**Callout / Alert Card**
- Dark surface variant: Magenta Pink (`#F80590`) background, White text, 8px radius, 16px 20px padding
- Light surface variant: Lavender Mist (`#E4DCF8`) background, Black text, 8px radius, 16px 20px padding
- No border, no shadow

### Inputs & Forms

**Dark Mode Input**
- Background: Ink Blue (`#080927`)
- Border: 1px solid Steel Blue (`#1D3B61`)
- Text: White (`#FFFFFF`), Arial 16px 400
- Placeholder: Ash Gray (`#82898D`)
- Padding: 12px 16px
- Radius: 6px
- Hover: border → Slate Blue (`#212353`), transition 0.2s ease
- Focus: border → Sky Blue (`#2398FF`), `box-shadow: 0 0 0 3px rgba(35,152,255,0.25)`
- Error: border → Tomato Red (`#FF464A`), `box-shadow: 0 0 0 3px rgba(255,70,74,0.25)`

**Light Mode Input**
- Background: White (`#FFFFFF`)
- Border: 1px solid Cool Gray (`#B9CDCB`)
- Text: Black (`#000000`), Arial 16px 400
- Placeholder: Ash Gray (`#82898D`)
- Padding: 12px 16px
- Radius: 6px
- Focus: border → Sky Blue (`#2398FF`), `box-shadow: 0 0 0 3px rgba(35,152,255,0.20)`
- Error: border → Tomato Red (`#FF464A`)

### Navigation

**Dark Navigation (primary)**
- Background: `rgba(13,15,32,0.95)`, backdrop-filter blur(12px)
- Border-bottom: 1px solid Steel Blue (`#1D3B61`)
- Logo: shield icon + "pilot" in White, "institute" in Sky Blue — standard lockup
- Nav links: White (`#FFFFFF`), Arial 13px weight 700, uppercase, letter-spacing 0.04em
- Active link: Sky Blue (`#2398FF`) text + 2px bottom border in Sky Blue
- Hover: Sky Blue text, transition 0.15s ease
- CTA button: Sky Blue primary button (right side)
- Sticky, z-index 100

**Light Navigation (editorial)**
- Background: White (`#FFFFFF`)
- Border-bottom: 1px solid Cool Gray (`#B9CDCB`)
- Logo: standard lockup, Black text variant
- Nav links: Black (`#000000`), Arial 13px weight 700, uppercase
- Hover: Sky Blue (`#2398FF`) text, transition 0.15s ease

---

## 5. Layout Principles

### Spacing Scale
Base unit: 8px

| Token | Value | Primary Use |
|-------|-------|-------------|
| space-1 | 4px | Micro gaps, icon padding |
| space-2 | 8px | Tight component gaps |
| space-3 | 12px | Compact element spacing |
| space-4 | 16px | Standard internal padding |
| space-5 | 24px | Card padding, form gaps |
| space-6 | 32px | Component group gap |
| space-7 | 40px | Sub-section spacing |
| space-8 | 48px | Section spacing (mobile) |
| space-9 | 64px | Section spacing (tablet) |
| space-10 | 80px | Section spacing (desktop) |
| space-11 | 96px | Major section breathing room |
| space-12 | 120px | Hero section vertical padding |

### Grid System
- Columns: 12
- Gutter: 24px
- Margin: 24px (mobile) → 40px (tablet) → auto (desktop)
- Max content width: 1140px
- Max container width: 1280px
- Full-bleed: 100vw — used for hero sections, dark alternating sections, video backgrounds

### Container Widths
- Text / editorial: 720px (optimal reading line length)
- Content: 960px
- Standard: 1140px
- Wide: 1280px
- Full-bleed: 100vw

### Whitespace Philosophy
**Command room pacing**: Dark sections breathe generously — 80–120px vertical padding between major blocks. This is not waste; it allows each content panel to register as a distinct instrument before the eye moves on. Crowding the dark surface reduces signal clarity. Light editorial sections use tighter spacing (40–64px) appropriate to document reading contexts.

### Border Radius Scale
| Name | Value | Use |
|------|-------|-----|
| Sharp | 0px | Data tables, full-bleed overlays |
| Micro | 4px | Inline badges, code chips |
| Standard | 6px | Buttons, inputs, small cards |
| Card | 12px | Standard cards, containers |
| Large | 16px | Featured cards, course tiles |
| Pill | 9999px | Status badges, filter tags |

---

## 6. Depth & Elevation

### Dark Mode Elevation

| Level | Name | Shadow | Use |
|-------|------|--------|-----|
| 0 | Ground | None — Midnight Navy + graph paper grid | Page canvas |
| 1 | Surface | 1px Steel Blue (`#1D3B61`) border, no shadow | Standard section containers |
| 2 | Raised | `0 4px 16px rgba(0,0,0,0.40)` | Default card elevation |
| 3 | Float | `0 8px 24px rgba(0,0,0,0.50)` | Hovered cards, dropdown menus |
| 4 | Overlay | `0 16px 48px rgba(0,0,0,0.60)` | Modals, drawers, popovers |

### Light Mode Elevation

| Level | Shadow | Use |
|-------|--------|-----|
| 1 | `0 1px 3px rgba(0,0,0,0.08)` | Resting card |
| 2 | `0 2px 8px rgba(0,0,0,0.10)` | Raised card |
| 3 | `0 4px 16px rgba(0,0,0,0.12)` | Hovered card |
| 4 | `0 8px 32px rgba(0,0,0,0.16)` | Modal |

**Graph paper as ground plane**: The single most powerful depth signal in the PI system is the graph paper grid — fine blue lines at 8% opacity on Midnight Navy. Content placed on this grid reads as elevated without any shadow. The grid is the ground; everything else floats above it. In multi-page print publications on white surfaces, the grid translates to a darker, lower-opacity line (e.g. Sky Blue at 6–10% or Black at 4–6%) — maintaining the technical, chart-like quality of the brand across both surface modes.

**Gradient as luminous elevation**: The Sky Blue → Magenta Pink gradient applied to course cards creates a sense of lit depth — as if content is illuminated from within. This is a PI-specific depth technique distinct from traditional shadows.

---

## 7. Do's and Don'ts

### Do
- Use Midnight Navy (`#0D0F20`) with the graph paper grid as the default design surface — this is the brand's home
- Use Sky Blue (`#2398FF`) as the primary interactive color — every link, CTA, and active state defaults here
- Use Magenta Pink (`#F80590`) with precision — it reads as a signal, not decoration; one per screen is usually enough
- Apply the Sky Blue → Magenta Pink gradient to hero and course imagery — it is the brand's most recognisable visual device
- Use Eina weight 500 for Display Hero and H2–H5 on light surfaces; use 400 for H1 and 300–400 on dark surfaces — weight responds to background contrast
- Reserve Gobold for 80px+ all-caps moments on dark surfaces only — treat it like an announcement, not a heading style
- Keep body text in Arial at 400 weight — Eina must not appear at paragraph size
- Use Forest Green (`#16A600`) for correct/pass states and Tomato Red (`#FF464A`) for incorrect/fail — these are established in PI's FAA quiz content
- Derive every color from `PI-Colour-Palette.csv` — no values outside the CSV are permitted
- Apply 80–96px vertical section padding in dark layouts — signal clarity requires breathing room

### Don't
- Don't use Magenta Pink as a fill for large content areas — it overwhelms at scale and reduces legibility
- Don't use Gobold below 60px or in mixed-case — it loses meaning and reads as a misapplied heading font
- Don't use Eina at body sizes (below 18px) — legibility degrades and the brand voice becomes confused
- Don't apply the graph paper grid to light surfaces in digital UI without purpose — in web and app contexts it is a dark-surface texture; on light surfaces it risks visual noise. Exception: multi-page print publications (study sheets, white papers, lead magnets) may use the grid on white backgrounds at very low opacity with a darker line color for a technical-document feel
- Don't use gradients on body text or UI labels — gradients are for imagery, card headers, and hero backgrounds
- Don't introduce hex values not present in the CSV — the palette is complete
- Don't reduce section padding below 48px on dark backgrounds — crowded dark surfaces lose their command-room quality
- Don't use Magenta Pink for inline body links — Sky Blue is the link color; Pink is reserved for alerts and accent moments
- Don't apply drop shadows to content on dark navy — shadows are invisible on dark backgrounds and must only be used in light-mode contexts
- Don't use cool blue-grays not in the CSV — the dark surface palette is precisely defined and must not drift

---

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <640px | Single column, stacked nav, reduced type scale |
| Tablet | 640px–1024px | 2-column grids, condensed nav, mid-scale type |
| Desktop | 1024px–1280px | Full layout, expanded nav, maximum typography |
| Wide | >1280px | Content locked at 1140px max-width, full-bleed sections stretch |

### Typography Scaling

| Role | Mobile | Tablet | Desktop |
|------|--------|--------|---------|
| Gobold Impact | 48px | 72px | 96px+ |
| Display Hero | 40px | 52px | 64px |
| H1 | 32px | 42px | 52px |
| H2 | 26px | 32px | 40px |
| H3 | 22px | 26px | 32px |
| H4 | 20px | 22px | 24px |
| Body | 16px | 16px | 16px |

### Layout Adaptations
- **Navigation**: Full horizontal nav → hamburger on mobile; logo + icon only visible; menu opens full-screen Midnight Navy overlay
- **Hero sections**: Centered single column on mobile; typography scales down progressively
- **Course cards**: 1-column (mobile) → 2-column (tablet) → 3-column (desktop)
- **Content grids**: 1-column → 2-column → 3–4-column
- **Section padding**: 48px (mobile) → 64px (tablet) → 96px (desktop)
- **Graph paper grid**: Remains on all screen sizes — it is identity, not decoration
- **Buttons**: Full-width on mobile for touch targets (min 44×44px for all interactive elements)

---

## 9. Agent Prompt Guide

### Quick Token Reference

| Category | Token | Value |
|----------|-------|-------|
| Page canvas (dark) | Midnight Navy | `#0D0F20` |
| Card surface (dark) | Ink Blue | `#080927` |
| Border (dark) | Steel Blue | `#1D3B61` |
| Primary action | Sky Blue | `#2398FF` |
| Hover state | Bright Blue | `#1877F2` |
| Signature accent | Magenta Pink | `#F80590` |
| Text on dark | White | `#FFFFFF` |
| Text on light | Black | `#000000` |
| Secondary text | Ash Gray | `#82898D` |
| Light page | White | `#FFFFFF` |
| Light card | Light Gray | `#F0F0F0` |
| Light border | Cool Gray | `#B9CDCB` |
| Brand gradient | — | `linear-gradient(135deg, #2398FF, #F80590)` |
| Grid texture | — | `rgba(35,152,255,0.08)` lines, 24px grid on `#0D0F20` |

### Example Prompts

**Hero section (dark):**
"Create a full-width hero on Midnight Navy (`#0D0F20`) with graph paper grid overlay — `linear-gradient(rgba(35,152,255,0.08) 1px, transparent 1px)` and `linear-gradient(90deg, rgba(35,152,255,0.08) 1px, transparent 1px)`, 24px grid size. Headline in Eina Bold 700 at 64px, White (`#FFFFFF`), line-height 1.00, letter-spacing -0.5px. Subtext in Arial 400 at 18px, White at 75% opacity, line-height 1.65. Primary CTA: Sky Blue (`#2398FF`) background, White text, Arial 13px 700 uppercase, 6px radius, 12px 24px padding. Secondary CTA: outline, Sky Blue border and text."

**Course card:**
"Design a course card with photography background and overlay `linear-gradient(to bottom, transparent 30%, #0D0F20 100%)`. Top accent: 3px border in `linear-gradient(135deg, #2398FF, #F80590)`. Radius 12px. Title: Eina SemiBold 600 at 20px, White. Category label: Arial 700 11px uppercase, Sky Blue (`#2398FF`). On hover: scale(1.02), shadow `0 8px 24px rgba(0,0,0,0.50)`, transition 0.25s ease."

**Feature card (dark):**
"Build a feature card on Ink Blue (`#080927`), 1px Steel Blue (`#1D3B61`) border, 12px radius, 24px padding, shadow `0 4px 16px rgba(0,0,0,0.40)`. Icon in Sky Blue (`#2398FF`). Title: Eina SemiBold 600 at 24px, White. Body: Arial 400 at 16px, White at 75% opacity, line-height 1.60. On hover: border → Sky Blue, shadow → `0 8px 24px rgba(0,0,0,0.50)`, transition 0.2s ease."

**Gobold impact section:**
"Full-bleed dark section on Midnight Navy (`#0D0F20`) with graph paper grid. Large Gobold Bold 700 at 96px, White (`#FFFFFF`), all-caps, line-height 0.92, letter-spacing -1px. Below: Arial 400 at 18px, White at 70% opacity, line-height 1.65. Gradient CTA button: `linear-gradient(135deg, #2398FF, #F80590)`, White text, Arial 13px 700 uppercase, 6px radius, 12px 28px padding."

**Primary button:**
"Button: Sky Blue (`#2398FF`) bg, White text, Arial 13px 700 uppercase letter-spacing 0.04em, 12px 24px padding, 6px radius. Hover: Bright Blue (`#1877F2`), 0.2s ease. Focus: 2px offset ring Sky Blue. Active: Bright Blue + `inset 0 2px 4px rgba(0,0,0,0.30)`."

**Editorial block (light mode):**
"Two-column layout on White (`#FFFFFF`). Section header: Eina Bold 700 at 32px, Black (`#000000`). Body: Arial 400 at 16px, Black, line-height 1.60. Callout box: Lavender Mist (`#E4DCF8`) background, 8px radius, 16px 20px padding, Black text. Table headers: Arial 700 13px uppercase, Sky Blue (`#2398FF`). Table borders: Cool Gray (`#B9CDCB`) 1px. Logo lockup bottom-left."

### Iteration Guide
1. Always name colors by token — "Sky Blue (`#2398FF`)" not "blue"
2. Always specify Eina weight — "Eina Bold 700" not just "Eina bold"
3. State the surface first — "on Midnight Navy with graph paper grid" or "on White"
4. Gobold only for 80px+ all-caps full-bleed moments — never for sub-headings
5. Specify both gradient endpoints and direction for every gradient use
6. The graph paper grid is never optional on dark surfaces — include it in every dark prompt
7. For states, specify: base → hover → focus → active in order
