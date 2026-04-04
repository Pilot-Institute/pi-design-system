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

## 2. Brand Foundation

> **This section is incomplete.** Vision, mission, values, and key audience descriptions are not present in the reference material and must be provided by the brand team before this section can be finalized.

### What belongs here
- **Vision**: The long-term aspirational statement for Pilot Institute
- **Mission**: What PI does and for whom, in one or two sentences
- **Core Values**: The principles that guide decisions, communications, and design choices
- **Key Audiences**: Primary and secondary audience profiles — who PI is designing for, their goals, and what they need from the brand

### Known brand orientation (from design guide)
Pilot Institute is the leading US online aviation groundschool — training drone pilots (Part 107), private pilots, and commercial aviation students. The brand communicates authority, clarity, and accessibility. It is not corporate, not startup-cool. It is a trusted instructor: confident, direct, energetic.

---

## 3. Logo System

### Logo Mark Anatomy

The Pilot Institute mark is a shield shape — a form that signals protection, authority, and credentialing authority directly relevant to the aviation certification context. The shield contains three structural elements:

- **Shield outer frame**: Sky Blue (`#2398FF`) — the primary brand blue defines the mark's perimeter
- **Wing elements**: Three Magenta Pink (`#F80590`) shapes extending to the left of the shield, forming a stylized flight symbol — wings in motion, suggesting both aircraft and forward momentum
- **Central star**: White (`#FFFFFF`) on dark backgrounds; Sky Blue (`#2398FF`) on light variant applications

The mark reads clearly at small sizes because the geometry is simple: a shield, a star, a directional wing burst. At large sizes, the wing shapes resolve into a distinct flight motif.

### Wordmark

The wordmark is "pilotinstitute" rendered as a single lowercase word — no space, no separator. This is a deliberate brand decision: "pilotinstitute" is a compound noun, not two words. The typographic treatment reinforces the distinction between the two syllable groups:

- **"pilot"**: set in the light/regular weight of Eina — conversational, approachable
- **"institute"**: set in the segment or brand primary color, matching the color context:
  - On dark backgrounds: "pilot" in White (`#FFFFFF`), "institute" in Sky Blue (`#2398FF`)
  - On light backgrounds: both words rendered in a dark indigo consistent with the brand's deep navy palette

**Important note on wordmark color values in SVG files**: The official logo SVG files use two hex values that do not appear in `PI-Colour-Palette.csv`:
- `#252e73` — used for the dark-mode wordmark color on light backgrounds. This is a logo-asset-specific value. The closest CSV equivalent for reference purposes is Electric Indigo (`#2E4292`), but `#252e73` must NOT be substituted. When reproducing the wordmark from the SVG file, use the SVG as the authoritative source. Do not use `#252e73` as a design token for any other element in the system.
- `#b8deff` — used for a light element in certain logo variants. The closest CSV equivalent for reference purposes is Baby Blue (`#81D1F4`), but `#b8deff` must NOT be substituted or used as a token. The SVG file is authoritative.

These values predate the CSV and represent the logo's pre-tokenized state. They are preserved as-is in the SVG assets. They must never be used outside the logo files.

### Logo Variants

**1. Horizontal Lockup (primary)**: Shield mark on the left, wordmark "pilotinstitute" to the right on the same baseline. This is the default usage for navigation bars, document headers, and any context where horizontal space permits.

**2. Mark Only**: The shield icon without the wordmark. Used when the brand is already established in context (e.g., favicon, app icon, social media profile image, watermarks on branded content). Not for use as a standalone brand identity on unbranded surfaces.

**3. Stacked**: Shield mark centered above the wordmark. Used when horizontal space is constrained and the mark-only variant is insufficient to establish context. Less common than the horizontal lockup.

### Color Modes

**Full Color on Dark (primary usage)**: The horizontal lockup with Sky Blue (`#2398FF`) shield, Magenta Pink (`#F80590`) wings, White (`#FFFFFF`) star, and dual-weight wordmark ("pilot" White, "institute" Sky Blue). Applied on Midnight Navy (`#0D0F20`) or any dark surface from the primary surfaces palette.

**Reversed / All-White on Dark or Color**: Single-color white logo on colored or photographic backgrounds where the full-color mark would compete with the background. Used sparingly.

**Dark Variant on Light**: Logo adapted for White (`#FFFFFF`) or Light Gray (`#F0F0F0`) backgrounds. The wordmark renders in dark indigo (SVG-specific value `#252e73` — see note above). Shield and wing colors retain their brand values as encoded in the SVG.

### Clear Space

The minimum clear space around the logo on all four sides equals the height of the shield icon in the horizontal lockup. No other graphic elements, text, image edges, or patterns may intrude on this zone. The graph paper grid texture may appear within the clear space zone only when the logo sits directly on the branded canvas (e.g., the nav bar on a grid-textured hero section).

### Minimum Size

- **Mark only**: 24px height minimum for digital use; 8mm minimum for print
- **Horizontal lockup**: 100px wide minimum for digital; 32mm wide minimum for print

Below these sizes, detail in the wings and star collapses and the mark loses its distinctiveness. Use the mark-only variant if the horizontal lockup would fall below minimum width.

### Visual Center & Alignment

Due to the asymmetrical design of the icon — the Magenta Pink wings extend significantly to the left of the shield — the logo's geometric bounding box center does not align with its visual center. The **visual center runs through the middle of the shield**, not the midpoint of the full bounding box (which sits further left, pulled by the wing shapes).

When placing or aligning the logo:
- **Centered layouts** (nav bars, hero sections, app icons): align to the visual center — the vertical axis through the middle of the shield — not the mathematical center of the bounding box. Centering on the bounding box will make the logo appear shifted to the right.
- **Left-aligned layouts**: align to the left edge of the wings (the true bounding box edge).
- **Right-aligned layouts**: align to the right edge of the shield / wordmark.

This applies to both the horizontal lockup and the mark-only variant. Optical centering on the shield always produces the correct result. Relying on the asset's bounding box for centering is a common error that should be avoided in all layout tools (Figma, CSS, After Effects, etc.).

### Logo Misuse Rules

Do NOT:
1. Stretch, compress, or distort the logo in any axis
2. Rotate the logo
3. Recolor any element using colors outside the defined logo color modes — do not apply segment colors to the shield or wings
4. Separate "pilot" and "institute" onto different lines or different typographic treatments not defined in this section
5. Add drop shadows, glows, or effects to any part of the logo
6. Place the logo on busy photographic backgrounds without sufficient contrast — always ensure the logo sits on a surface or overlay that provides clear legibility
7. Use the mark-only variant as a standalone brand identity on unbranded surfaces where the brand has not been established by other means
8. Reproduce the wordmark using any font other than the official Eina-based SVG artwork

---

## 4. Color Palette & Roles

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
- **Deep Teal** (`#000F17`): The absolute darkest surface — used only for the most immersive full-bleed dark environments.
- **Electric Indigo** (`#2E4292`): Mid-dark surface, background for interactive chart elements and feature grids. Also the closest CSV equivalent to the logo's off-palette wordmark value `#252e73`.

### Primary Interactive
- **Sky Blue** (`#2398FF`): The primary brand blue — primary CTAs, active links, interactive highlights, icon fills, table headers in light mode, and the origin point of the brand gradient. The single most-used chromatic color.
- **Bright Blue** (`#1877F2`): Hover and pressed state for Sky Blue interactive elements. Slightly deeper for visible feedback.
- **Magenta Pink** (`#F80590`): The signature brand accent — secondary CTAs, alert indicators, gradient terminus, callout backgrounds. Used with precision; never as a fill for large content areas.

### Light Surfaces (Editorial / Print Mode)
- **White** (`#FFFFFF`): Primary light page background — study sheets, white papers, the light preview mode.
- **Light Gray** (`#F0F0F0`): Alternate light background, card surface on white layouts, icon container background in light mode.
- **Ivory** (`#FFF5E5`): Warm light card surface.
- **Linen** (`#F3ECD9`): Warm neutral callout area background in print layouts.
- **Cream** (`#FFF0D0`): Warmest light tint, used rarely in digital contexts.

### Text
- **White** (`#FFFFFF`): Primary text on all dark surfaces.
- **Black** (`#000000`): Primary text on all light surfaces.
- **Ash Gray** (`#82898D`): Secondary and caption text on light surfaces. Placeholder text in inputs.
- **Cool Gray** (`#B9CDCB`): Tertiary text, metadata, and de-emphasised labels on light surfaces. Also used as border color on light layouts.

### Semantic States
- **Forest Green** (`#16A600`): Correct answer, pass state, success — the primary right/correct indicator in FAA and quiz content.
- **Lime Green** (`#63DB00`): Secondary success, strong completion badge.
- **Seafoam Green** (`#2AEAA7`): Soft success surface tint, progress completion. Also a primary illustration palette color.
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
- **Lavender Purple** (`#8759F2`): Secondary illustration accent, chart series 2. Primary illustration character color.
- **Aqua Blue** (`#0EBFE5`): Tertiary accent for data visualisation and infographics, chart series 3. Primary illustration character color.
- **Cyan Sky** (`#5AD7ED`): Illustration highlight, chart series 4.
- **Turquoise** (`#3EBBD4`): Map and geography visualisations.
- **Ocean Blue** (`#029DCD`): Informational chart fills.
- **Baby Blue** (`#81D1F4`): Icon background tint, light blue chip. Closest CSV equivalent to logo off-palette value `#b8deff`.
- **Cerulean** (`#33A7F2`): Link hover on light surfaces.
- **Fuchsia** (`#E42A84`): Deep pink, hover state for Magenta Pink CTAs, gradient midpoint variant.
- **Deep Magenta** (`#B9006E`): Deep pink accent for high-contrast moments.
- **Royal Purple** (`#7F1C7D`): Illustration accent, chart series color.
- **Lavender Mist** (`#E4DCF8`): Light badge background and callout surface on white layouts.
- **Coral** (`#ED683D`): Warmer warning variant.
- **Peach** (`#F6BC86`): Illustration warm tint.
- **Blush** (`#F5ACA5`): Light pink illustration tint.
- **Brown** (`#663300`): Warm earth illustration accent.

### Gradient System
The PI gradient runs **Sky Blue** (`#2398FF`) → **Magenta Pink** (`#F80590`) at 135°. It represents the brand's arc from technical clarity to energetic action. Applied to: course card overlays, hero section accents, and gradient CTA buttons. A secondary gradient Sky Blue → **Lavender Purple** (`#8759F2`) is used for calmer informational contexts. Neither gradient is applied to text or UI labels.

---

## 5. Typography Rules

### Font Families
- **Display / Headline**: `Eina`, fallback: `Arial, system-ui, -apple-system, 'Helvetica Neue', sans-serif`
- **Impact**: `Gobold`, fallback: `'Arial Black', Impact, sans-serif`
- **Body / UI**: `Arial`, fallback: `system-ui, -apple-system, 'Helvetica Neue', sans-serif`

*Eina is a licensed geometric sans-serif with Regular, SemiBold, Bold, and Italic variants. When unavailable, use Arial — do not substitute Montserrat, Futura, or other geometric fonts, as they alter the brand's proportions. Gobold is a condensed bold display font used exclusively in all-caps at large display sizes.*

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Usage |
|------|------|------|--------|-------------|----------------|-------|
| Gobold Impact | Gobold | 80–120px (5–7.5rem) | 700 | 1.2 | 0 | Full-bleed dark section callouts, video text overlays. All-caps only. |
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

## 6. Photography

### Photography Types and Subject Categories

**Course Photography**: Real aviation scenes — cockpit interiors with students and instructors, aircraft in flight from aerial perspectives, runway sequences, instructor-student interactions at controls or preflight. These images establish the teaching context and signal the real-world application of course content.

**Hero Section Photography**: Full-bleed photography used as section backgrounds, always with a gradient or color overlay treatment. Subject matter ranges from cockpit interiors to wide aerial vistas. The photography is never the primary surface — the overlay brings it into the PI brand environment.

**Lead Magnet and Cover Photography**: Dramatic overhead or bird's-eye perspective photography of aircraft — the most distinctive PI composition signature. A white Cessna photographed from directly above, wings spread against a Midnight Navy (`#0D0F20`) background with a graph paper grid overlay, is the archetypal PI lead magnet image. This dramatic angle and the pairing of photography with the branded surface creates a visual that is unmistakably PI even without the logo.

**YouTube Thumbnails**: Instructor or host portraits in front of aviation backdrops, or aircraft photography with text overlay. High energy, direct eye contact, readable at small sizes.

### Photography Style Rules

- **Contrast and saturation**: High contrast, saturated images — not flat or desaturated. Aviation environments are rich in detail and color; the photography should reflect this with clarity.
- **Authenticity**: Real aircraft, real environments, real instructors. Generic stock photography of people at computers or abstract light trails is not acceptable. If it could illustrate a non-aviation business, it does not belong.
- **Color temperature**: Neutral to slightly cool — matching the blue-dominant brand palette. Warm golden-hour images are acceptable only when paired with appropriately cool overlay treatments.
- **Scale and drama**: Photography should communicate scale — the vastness of sky, the precision of instruments, the complexity of a cockpit. Tight, unrevealing crops lose the aviation context.
- **Overhead perspective**: The bird's-eye view is a PI signature for lead magnet and cover images. Aircraft photographed from above with the ground or a branded surface visible below register as distinctively PI.

### Photography Treatments

Photography is never placed bare on a white background in digital UI contexts. Every photography application in UI receives a surface treatment:

**Course Card Overlay**:
`linear-gradient(to bottom, transparent 30%, #0D0F20 100%)`
Applied over course photography in card layouts. The bottom fade anchors the card text on the Midnight Navy surface color. Token names: transparent → Midnight Navy (`#0D0F20`).

**Hero Section Overlay**:
`linear-gradient(135deg, rgba(35,152,255,0.30), rgba(248,5,144,0.30))`
Applied over full-bleed hero photography. The diagonal blue-to-pink gradient references the brand gradient while keeping the photography readable beneath. Based on: Sky Blue (`#2398FF`) at 30% opacity → Magenta Pink (`#F80590`) at 30% opacity.

**Lead Magnet Cover Treatment**:
Photography placed on Midnight Navy (`#0D0F20`) background with graph paper grid overlay. Often photographed at a dramatic overhead angle. The grid is rendered at the standard 24px grid size, `rgba(35,152,255,0.08)` line color, consistent with the signature canvas treatment. Based on: Sky Blue (`#2398FF`) at 8% opacity grid lines.

### Photography Don'ts

- Do not place photography on a bare white background in digital UI — always apply a surface treatment
- Do not use photography that does not include real aviation subjects — cockpits, aircraft, runways, aviation equipment, or clearly aviation-context humans
- Do not use warm-toned photography without a compensating cool overlay treatment
- Do not crop photography so tightly that the aviation context is lost
- Do not use photography that reads as generic corporate stock — the test is whether the image could illustrate a non-aviation subject
- Do not stretch, distort, or pixelate photography at any usage size — maintain aspect ratios and supply sufficient resolution

---

## 7. Illustration & Icons

### Illustration Style

PI illustration is flat vector — simplified geometry, no photorealism, no gradients within illustration fills, no complex textures. The style sits at the intersection of technical diagram and editorial cartoon: precise enough to read as professional, simplified enough to feel approachable.

### Character Rules

**Form**: Simplified humanoid figures with oval or round heads and minimal facial features. Bodies are stylized — no complex anatomical detail. Facial features are present but reduced: eyes as simple shapes, no detailed expressions.

**Aviation Theme**: Characters wear aviation-appropriate items — headsets, pilot uniforms, hi-vis vests, drone controller harnesses. The aviation context must be legible from the illustration without text support.

**Color Limit**: No more than two to three brand colors per character figure. Characters should be filled with colors from the Illustration Palette below. Background elements may use additional palette colors, but the figure itself remains high-contrast and readable.

**Poses**: Standing, pointing at displays or charts, operating instruments, seated at cockpit controls, demonstrating procedures. Poses communicate active learning and professional competence.

**Background**: On Midnight Navy (`#0D0F20`) with graph paper grid overlay as the primary illustration context (dark mode). On White (`#FFFFFF`) for editorial/print illustration contexts.

### Illustration Color Palette (Character Fills)

The primary character illustration colors in order of priority:

| Token | Hex | Role |
|-------|-----|------|
| Sky Blue | `#2398FF` | Primary figure fill — the dominant character color |
| Magenta Pink | `#F80590` | Secondary accent — headset, equipment details, emphasis elements |
| Lavender Purple | `#8759F2` | Tertiary figure fill — second character or secondary clothing area |
| Aqua Blue | `#0EBFE5` | Equipment highlight, instrument glow effects |
| Seafoam Green | `#2AEAA7` | Accent detail, status indicators, positive-state elements |

Additional illustration-safe colors from the CSV (used for environment and equipment, not character fills):
- Turquoise (`#3EBBD4`), Ocean Blue (`#029DCD`), Cerulean (`#33A7F2`) for map and environment fills
- Peach (`#F6BC86`), Blush (`#F5ACA5`) for skin-tone approximations where needed
- White (`#FFFFFF`) for highlights, star shapes, instrument screens
- Golden Yellow (`#FFBE33`) for warning indicators and star/badge shapes

### Equipment and Environment Illustrations

- **Drones**: Simplified top-down and 3/4-view flat vectors. Quadcopter form with four arms and rotors. Filled in Midnight Navy (`#0D0F20`) or Sky Blue (`#2398FF`) depending on the surface.
- **Fixed-wing aircraft**: Simplified silhouettes — overhead view showing wingspan, tail, fuselage. Used as category identifiers for the Airplanes segment.
- **Helicopters**: Simplified profile silhouette — main rotor, tail rotor, cabin. Used as category identifier for the Helicopters segment.
- **Instrument panels**: Flat representation of cockpit instruments — simplified circles and dials. Fills in Slate Blue (`#212353`) and Steel Blue (`#1D3B61`) for the panel, Sky Blue (`#2398FF`) and Golden Yellow (`#FFBE33`) for active instruments.
- **Aviation charts and maps**: Stylized US maps with Turquoise (`#3EBBD4`) and Ocean Blue (`#029DCD`) fills for geographic data. Route markers and waypoints in Sky Blue (`#2398FF`) and Magenta Pink (`#F80590`).

### Infographic Color Usage

Data series colors in order: Sky Blue (`#2398FF`), Magenta Pink (`#F80590`), Lavender Purple (`#8759F2`), Aqua Blue (`#0EBFE5`), Seafoam Green (`#2AEAA7`). Pie and donut charts use the same series. Never use colors outside the CSV palette for chart fills.

### Illustration Don'ts

- No photorealistic illustration — all illustration must be flat vector
- No gradient fills within illustration elements — gradients are for photography overlays and CTA buttons only
- No complex textures within illustration shapes
- No colors outside the CSV palette — if a color is not in `PI-Colour-Palette.csv`, it cannot appear in any illustration
- No more than three colors per character figure
- No illustration in light mode contexts without verifying contrast — Sky Blue figures on White must have sufficient contrast; add Midnight Navy outlines if needed

### Icon System

**Style**: Flat, filled or line, consistent geometric weight. Icons use simple 2px stroke for line variants or flat fill for solid variants. No realistic or pseudo-3D treatment.

**Size Scale**:

| Token | Size | Usage |
|-------|------|-------|
| Icon-XS | 16px | Inline with text, metadata labels |
| Icon-SM | 20px | UI elements, buttons with icon |
| Icon-MD | 24px | Feature lists, card icons |
| Icon-LG | 32px | Section feature icons |
| Icon-XL | 48px | Hero feature icons, large displays |

**Color on Dark Surfaces**: Sky Blue (`#2398FF`) icon fill. Container: optional circle with Ink Blue (`#080927`) background.

**Color on Light Surfaces**: Midnight Navy (`#0D0F20`) or Black (`#000000`) icon fill. Container: optional circle with Light Gray (`#F0F0F0`) background.

**Aviation Category Icons**:
- Fixed-wing airplane silhouette — Airplanes segment identifier
- Quadcopter drone silhouette — Drones segment identifier
- Helicopter silhouette — Helicopters segment identifier

**Functional Icons**: Chevron (right, down, left, up), checkmark, close/X, search (magnifying glass), menu (three horizontal lines), external link (box with arrow), download (arrow down to line), play button (filled triangle).

**Status Icons**:
- Circle-check: Forest Green (`#16A600`) — success, correct, pass
- Circle-X: Tomato Red (`#FF464A`) — error, incorrect, fail
- Circle-exclamation: Orange (`#FF6600`) — warning, caution
- Circle-i: Sky Blue (`#2398FF`) — information, tip

**Icon Don'ts**:
- Do not use icons outside the defined size scale
- Do not mix fill and line style within the same composition
- Do not use icon colors outside the defined on-dark or on-light rules — no ad-hoc icon coloring
- Do not place Midnight Navy icons on dark surfaces — they disappear
- Do not place Sky Blue icons on White without verifying the 3:1 minimum contrast ratio for UI icons

---

## 8. Component Stylings

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
- Background: `linear-gradient(135deg, #2398FF, #F80590)` — Sky Blue → Magenta Pink
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
- Logo: horizontal lockup — "pilot" White, "institute" Sky Blue
- Nav links: White (`#FFFFFF`), Arial 13px weight 700, uppercase, letter-spacing 0.04em
- Active link: Sky Blue (`#2398FF`) text + 2px bottom border in Sky Blue
- Hover: Sky Blue text, transition 0.15s ease
- CTA button: Sky Blue primary button (right side)
- Sticky, z-index 100

**Light Navigation (editorial)**
- Background: White (`#FFFFFF`)
- Border-bottom: 1px solid Cool Gray (`#B9CDCB`)
- Logo: dark variant horizontal lockup
- Nav links: Black (`#000000`), Arial 13px weight 700, uppercase
- Hover: Sky Blue (`#2398FF`) text, transition 0.15s ease

---

## 9. Layout Principles

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

## 10. Depth & Elevation

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

## 11. Do's and Don'ts

### Do

1. Use Midnight Navy (`#0D0F20`) with the graph paper grid as the default design surface — this is the brand's home. Every dark-mode layout begins here.
2. Use Sky Blue (`#2398FF`) as the primary interactive color — every link, CTA, and active state defaults to this token.
3. Use Magenta Pink (`#F80590`) with precision — it reads as a signal, not decoration; one prominent Magenta Pink element per screen is usually enough.
4. Apply the Sky Blue → Magenta Pink gradient to hero and course imagery — it is the brand's most recognisable visual device.
5. Use Eina weight 500 for Display Hero and H2–H5 on light surfaces; use 300–400 on dark surfaces — weight adjusts to surface contrast.
6. Reserve Gobold for 80px+ all-caps moments on dark surfaces only — treat it like a public address announcement, not a heading style.
7. Derive every color from `PI-Colour-Palette.csv` without exception — the palette is complete.
8. Apply photography treatments (gradient overlays) to all photography used in digital UI — bare photography never sits on a white background in product contexts.
9. Use Forest Green (`#16A600`) for correct/pass states and Tomato Red (`#FF464A`) for incorrect/fail — these are established in PI's FAA quiz content and must be consistent.
10. Apply 80–96px vertical section padding in dark layouts — signal clarity requires breathing room.
11. Reproduce the logo from the official SVG assets — never redraw or recreate it from memory.
12. Limit illustration character figures to two to three brand colors maximum — character legibility depends on color restraint.

### Don't

1. Do not use Magenta Pink (`#F80590`) as a fill for large content areas — it overwhelms at scale and reduces legibility.
2. Do not use Gobold below 60px or in mixed-case — it loses its announcement quality and reads as a misapplied heading font.
3. Do not use Eina at body sizes (below 18px) — legibility degrades and the brand voice becomes confused. Arial is the body font without exception.
4. Do not apply the graph paper grid to light surfaces in digital UI without purpose — it is a dark-surface texture. Exception: multi-page print publications may use the grid on white at very low opacity.
5. Do not use gradients on body text or UI labels — gradients are for photography overlays, card headers, and hero backgrounds only.
6. Do not introduce hex values not present in the CSV — the only permitted off-palette values are `#252e73` and `#b8deff` within the logo SVG files only.
7. Do not reduce section padding below 48px on dark backgrounds — crowded dark surfaces lose their command-room quality.
8. Do not use Magenta Pink for inline body links — Sky Blue (`#2398FF`) is the link color; Pink is reserved for alerts, CTAs, and accent moments.
9. Do not apply drop shadows to content on dark navy — shadows are invisible on dark backgrounds; use border or elevation color shifts instead.
10. Do not place photography on a bare white background in digital UI — always apply a gradient overlay or surface treatment.
11. Do not recolor logo elements with segment colors or off-brand values — use only the defined logo color modes from Section 3.
12. Do not use illustration gradient fills — all illustration fills must be flat color from the CSV palette.

---

## 12. Responsive Behavior

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
- **Logo**: Full horizontal lockup on desktop and tablet; mark-only acceptable on mobile in nav context if horizontal space is critically constrained

---

## 13. Agent Prompt Guide

### Quick Token Reference

| Category | Token | Value |
|----------|-------|-------|
| Page canvas (dark) | Midnight Navy | `#0D0F20` |
| Card surface (dark) | Ink Blue | `#080927` |
| Border (dark) | Steel Blue | `#1D3B61` |
| Primary action | Sky Blue | `#2398FF` |
| Hover state | Bright Blue | `#1877F2` |
| Signature accent | Magenta Pink | `#F80590` |
| Pink hover | Fuchsia | `#E42A84` |
| Text on dark | White | `#FFFFFF` |
| Text on light | Black | `#000000` |
| Secondary text | Ash Gray | `#82898D` |
| Light page | White | `#FFFFFF` |
| Light card | Light Gray | `#F0F0F0` |
| Light border | Cool Gray | `#B9CDCB` |
| Illustration 1 | Sky Blue | `#2398FF` |
| Illustration 2 | Magenta Pink | `#F80590` |
| Illustration 3 | Lavender Purple | `#8759F2` |
| Illustration 4 | Aqua Blue | `#0EBFE5` |
| Illustration 5 | Seafoam Green | `#2AEAA7` |
| Icon container (dark) | Ink Blue | `#080927` |
| Icon container (light) | Light Gray | `#F0F0F0` |
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
"Two-column layout on White (`#FFFFFF`). Section header: Eina Bold 700 at 32px, Black (`#000000`). Body: Arial 400 at 16px, Black, line-height 1.60. Callout box: Lavender Mist (`#E4DCF8`) background, 8px radius, 16px 20px padding, Black text. Table headers: Arial 700 13px uppercase, Sky Blue (`#2398FF`). Table borders: Cool Gray (`#B9CDCB`) 1px. Logo lockup bottom-left, dark variant."

**Logo placement (dark nav):**
"Place the horizontal logo lockup in the nav left position using `../reference/img/PI_logo_hor-light.svg` at 26px height. Nav background: `rgba(13,15,32,0.95)` with backdrop-filter blur(12px). Border-bottom: 1px solid Steel Blue (`#1D3B61`). The SVG encodes the shield in Sky Blue (`#2398FF`), wings in Magenta Pink (`#F80590`), star in White (`#FFFFFF`), wordmark in White. Maintain clear space equal to the shield height on all sides of the logo. Do not stretch or recolor any element."

**Logo placement (light header):**
"Place the dark horizontal logo lockup using `../reference/img/PI_logo_hor-dark.svg` at 26px height in the top-left of a White (`#FFFFFF`) page header. The SVG wordmark uses `#252e73` for the dark-mode text — this is a logo-asset-specific value not in the token system; do not apply it elsewhere. Nav border-bottom: 1px solid Cool Gray (`#B9CDCB`). Nav links: Black (`#000000`), Arial 13px 700 uppercase. CTA: Sky Blue (`#2398FF`) primary button."

**Illustration character (dark surface):**
"Create a flat vector character on Midnight Navy (`#0D0F20`) with graph paper grid overlay. Character: simplified oval head, stylized body wearing a pilot headset. Primary fill: Sky Blue (`#2398FF`). Headset and detail accent: Magenta Pink (`#F80590`). Maximum three colors on the figure. No gradients within the character fills — flat vector only. No photorealistic features. Pose: standing, one arm gesturing toward a chart or instrument. Background includes stylized aviation chart lines in Aqua Blue (`#0EBFE5`) at 30% opacity."

**Icon usage (dark surface):**
"Render a 24px checkmark icon in Sky Blue (`#2398FF`) within a 40px circle container using Ink Blue (`#080927`) background, on a Midnight Navy (`#0D0F20`) card surface. Status icon for correct answer state: use Forest Green (`#16A600`) circle-check at 20px. Status icon for error state: Tomato Red (`#FF464A`) circle-X at 20px. All icons are flat, filled, consistent weight. No drop shadows on dark surfaces."

**Photography overlay (hero):**
"Full-bleed hero section: aviation cockpit photography at 100vw width. Over the photography, apply `linear-gradient(135deg, rgba(35,152,255,0.30), rgba(248,5,144,0.30))` — Sky Blue (`#2398FF`) at 30% → Magenta Pink (`#F80590`) at 30%, 135 degrees. On top of the overlay: Eina 400 at 64px, White (`#FFFFFF`), line-height 1.00. The photography must be real aviation subject matter — cockpit interior with instruments visible. Do not use generic stock."

### Iteration Guide
1. Always name colors by token — "Sky Blue (`#2398FF`)" not "blue"
2. Always specify Eina weight — "Eina Bold 700" not just "Eina bold"
3. State the surface first — "on Midnight Navy with graph paper grid" or "on White"
4. Gobold only for 80px+ all-caps full-bleed moments — never for sub-headings
5. Specify both gradient endpoints and direction for every gradient use
6. The graph paper grid is never optional on dark surfaces — include it in every dark prompt
7. For states, specify: base → hover → focus → active in order
8. For logo placements, reference the SVG file path and specify which variant (light/dark), never describe recoloring
9. For illustration, specify the surface, the character color limit, and confirm flat vector with no gradients
10. For icons, specify: size token, color token, container color token, and surface — in that order
