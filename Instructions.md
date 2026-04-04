# PI Design System — Claude Instructions

---

## Repository Architecture

This repository is the operational design infrastructure for Pilot Institute. It enables Claude, designers, and engineers to produce brand-consistent assets across all output types.

```
PI-design-system/
├── reference/
│   ├── PI-Colour-Palette.csv     ← color source of truth (auto-synced from Google Sheets)
│   ├── instructions.md           ← prompt for regenerating design-system/ files
│   └── img/                      ← design guide reference images and logo SVG files
├── design-system/                ← core tokens (typography, spacing, components, elevation)
│   ├── DESIGN.md
│   ├── preview.html
│   ├── preview-dark.html
│   └── README.md
├── segments/                     ← brand segment overrides (primary color per segment)
│   ├── airplanes.md
│   ├── drones.md
│   ├── helicopters.md
│   └── flight-attendant.md
├── modules/                      ← output-specific format specs
│   ├── video/
│   ├── graphics/
│   │   ├── social-media/
│   │   ├── editorial/
│   │   └── events/
│   ├── ads/
│   ├── 2d-animation.md
│   ├── 3d-animation.md
│   └── troubleshooting-guides.md
├── notes/                        ← session notes created by /note command
└── .github/workflows/
    └── sync-colour-palette.yml   ← daily Google Sheets → CSV sync
```

---

## Mandatory Reading Order

When generating any design asset, always read sources in this exact order:

1. **`reference/PI-Colour-Palette.csv`** — all permitted colors. Never invent, approximate, or substitute.
2. **`reference/img/`** — read all design guide images AND all SVG logo files (see Source Material below).
3. **`design-system/DESIGN.md`** — base tokens: typography, spacing, components, elevation, logo system, photography, illustration, and icon rules.
4. **`segments/{segment}.md`** — if a segment is specified, apply its overrides on top of the base.
5. **`modules/{category}/{module}.md`** — format-specific rules for the output being produced.

If any file is a stub or empty, skip it and proceed with what is available. Never block on a missing file.

---

## Segments

Pilot Institute organizes content into brand segments. Each segment has one primary color that visually identifies it across all output types. All other tokens inherit from `design-system/DESIGN.md`.

| Segment | Primary Color | Token Name | Hex |
|---|---|---|---|
| Airplanes | Blue | Sky Blue | `#2398FF` |
| Drones | Pink | Magenta Pink | `#F80590` |
| Helicopters | Dark Indigo | Electric Indigo | `#2E4292` |
| Flight Attendant | Purple (gradient) | Lavender Purple → Rich Purple | `#8759F2` → `#3A0256` |

When no segment is specified, default to Airplanes.

---

## Change Management

| What changed | Where to make the change | What is affected |
|---|---|---|
| Color value | Edit Google Sheet → auto-syncs to CSV | All files using that token |
| Base token (type, spacing, component) | `design-system/DESIGN.md` | All modules |
| Segment primary color | `segments/{segment}.md` | All outputs for that segment |
| Module-specific rule | `modules/{category}/{module}.md` | That module only |
| New segment | Add `segments/{name}.md` | Nothing else changes |
| New module | Add `modules/{category}/{name}.md` | Nothing else changes |

---

## Rules Claude Must Always Follow

1. Every color used must trace back to a row in `PI-Colour-Palette.csv`. No exceptions. The only permitted off-CSV hex values are `#252e73` and `#b8deff`, which exist exclusively within the logo SVG asset files — they must never be used as design tokens or applied outside the logo.
2. Never use vague color descriptors ("blue", "dark") — always use the semantic token name.
3. Never redefine a base token in a module unless the design guide explicitly requires it.
4. When a segment is specified, apply its primary color override before reading the module.
5. When a module file is a stub, apply defaults from `design-system/DESIGN.md` and flag the gap.
6. If the output reads like a generic UI kit, it has failed. Every output must feel like Pilot Institute.

---

## Role

You are a senior brand systems architect and AI design specification writer. Your job is to create production-grade design system files that allow Claude, designers, and engineers to apply Pilot Institute branding consistently and accurately across digital artefacts. You do not write generic style guides. You produce operational design infrastructure that can guide UI generation, be visually validated in HTML, and express clear design intent.

---

## Task

Generate exactly four files, written to `design-system/`:

| File | Description |
|------|-------------|
| `design-system/DESIGN.md` | Complete 13-section design specification |
| `design-system/preview.html` | Light mode visual token catalog |
| `design-system/preview-dark.html` | Dark mode visual token catalog |
| `design-system/README.md` | System overview and usage notes |

All four files must be internally consistent and production-ready. Do not modify anything in `reference/` or `modules/`.

---

## Source Material

Read all of the following before generating any output. Do not skip any source.

### Color palette (primary source of truth)
Read the `.csv` file in `reference/`. This is the **only** authoritative source for all color values. See the Color Rules section below.

### Design guide images
Read all images in `reference/img/`. They are exports from the official Pilot Institute Design Guide and cover: color system, typeface specimens, logo variants, visual devices, illustration style, course UI, lead magnet layouts, white paper templates, and design system structure.

### SVG logo files
Read the SVG logo files in `reference/img/`. The primary files are:
- `PI_logo_hor-dark.svg` — horizontal lockup for light backgrounds (dark wordmark)
- `PI_logo_hor-light.svg` — horizontal lockup for dark backgrounds (light/white wordmark)
- Any mark-only or stacked variant SVGs present in the same directory

When reading these SVGs, extract and document the exact color values used in the paths. Note that two hex values in these files — `#252e73` (dark wordmark) and `#b8deff` (light element) — do not appear in `PI-Colour-Palette.csv`. These are pre-existing logo-asset-specific values. Do not use them as design tokens. Flag them explicitly in the Logo System section of DESIGN.md as logo-internal values that exist outside the token system.

### Real-world output samples
Read all `.jpg` and `.png` files in `reference/img/` that are not design guide exports. These show the brand applied to actual print and digital artifacts.

### Branding prompts
Read all `.md` files in `reference/branding/`. These contain established brand application rules for thumbnails, charts, and other outputs — treat them as confirmed brand decisions.

### Website screencaptures
Read all files in `reference/website/`, loading pages 1–3 of each. These show the live brand in its primary digital context.

### Format reference
Read all files in `reference/output-examples/`. These are benchmark-quality design system outputs (Claude and Apple). Your PI output must reach the same depth, specificity, and structural quality.

---

## Color Rules

**`PI-Colour-Palette.csv` is the single source of truth for all colors.**

- Before generating any output, read and parse the CSV in full
- Every color token used across all four output files must trace back to a row in that CSV
- Use the `HEX` column as the authoritative value; if a row has no HEX, derive it from `RGB` then `CMYK`
- Use the `Name` column verbatim as the semantic token name
- Do not invent, approximate, or substitute colors not present in the CSV
- Do not hard-code any color value that does not appear in the CSV
- The only permitted exceptions are `#252e73` and `#b8deff` — logo SVG asset values, documented in Section 3 of DESIGN.md only, never used as design tokens
- When the CSV is updated and the prompt is re-run, all four output files must reflect the updated palette without requiring changes to this file

---

## Brand Context

Use this as orientation. Always verify specifics against the source images and CSV above.

### Identity
Pilot Institute is the leading US online aviation groundschool — training drone pilots (Part 107), private pilots, and commercial aviation students. The brand communicates authority, clarity, and accessibility. It is not corporate, not startup-cool. It is a trusted instructor: confident, direct, energetic.

### Visual Atmosphere
A command-centre surface — deep navy with a graph paper grid overlay that evokes aviation charts and technical precision. Bright electric blue and magenta pink cut through the dark background like instrument panel lights. The experience is high-contrast, purposeful, and slightly kinetic — as if the content is always ready to launch.

### Typography

| Font | Role |
|------|------|
| Eina | Display and headlines — geometric sans-serif. Weights: Regular, SemiBold, Bold, Italic |
| Gobold | Impact statements — condensed bold display, all-caps only, used sparingly |
| Arial | Body copy, UI, labels, navigation — system fallback for all functional text |

Fallback stack: `Arial, system-ui, -apple-system, 'Helvetica Neue', sans-serif`

### Key Design Characteristics
- **Graph paper grid** on dark navy backgrounds — signature texture, not decoration
- **Dark-first**: the primary design surface is dark navy, not white
- **High-contrast pairing**: Blue + Pink on Navy is the core brand combination
- **Flat vector illustration** style — simplified characters in brand colors, aviation-themed
- **Editorial boldness**: large overlapping type, text that bleeds out of containers in dark sections
- **Clean two-column layout** for print and editorial (white background, Sky Blue accent headers)
- **Gradient treatments**: blue-to-pink linear gradients on hero imagery and course cards
- **Logo**: shield with wings and star; "pilot" in white (light weight), "institute" in Sky Blue

---

## DESIGN.md — Required Sections

Must include all 13 sections. No omissions.

### 1. Visual Theme & Atmosphere
- Use material, emotional, or real-world analogies to describe the visual identity
- Avoid all generic descriptors: "clean", "modern", "minimal" are not permitted
- Each characteristic must feel distinctively Pilot Institute — not interchangeable with any other brand

### 2. Brand Foundation
- Vision, mission, core values, key audiences
- If source material does not supply these, write a clearly marked placeholder directing the brand team to supply the content
- Include a "known brand orientation" summary derived from available reference material

### 3. Logo System
- Logo mark anatomy: shield shape, wings, star, color breakdown
- Wordmark: "pilotinstitute" as single word, weight treatment for "pilot" vs "institute"
- Logo variants: horizontal lockup (primary), mark-only, stacked
- Color modes: full color on dark, reversed on dark/color, dark variant on light
- Clear space rules: minimum clear space measurement
- Minimum size rules: mark and horizontal lockup
- SVG asset values: document `#252e73` and `#b8deff` as logo-asset-specific, outside token system
- Visual center note: the icon is asymmetrical — wings extend left, so the visual center runs through the middle of the shield, not the bounding box center. Document alignment rules for centered, left-aligned, and right-aligned placements. Warn against using bounding box center for optical alignment.
- Misuse rules: at least 6 explicit don'ts

### 4. Color Palette & Roles
- All colors sourced exclusively from the CSV — no exceptions
- Every entry must include: semantic name (verbatim from CSV), hex value, functional role, usage context
- Group into logical systems: primary surfaces, interactive, text, borders, semantic states, illustration accents
- Explain the rationale for each role assignment

### 5. Typography Rules
- Full hierarchy table: font family, size (px and rem), weight, line height, letter spacing, usage context
- Must cover: display/hero, multiple heading levels, body (large, standard, small), labels, captions, micro, code
- Include typographic philosophy

### 6. Photography
- Photography types and subject categories: course photography, hero sections, lead magnet covers, YouTube thumbnails
- Style rules: contrast, saturation, color temperature, authenticity requirements
- Photography treatments: specific overlay gradient values with named tokens
- Placement rules: when photography appears vs. does not appear
- Photography don'ts

### 7. Illustration & Icons
- Illustration style: flat vector, geometry rules, no photorealism
- Character rules: head/body shapes, features, colors (limit per figure), poses and aviation themes
- Equipment and icon illustrations
- Color rules for illustration (CSV-only palette enforcement)
- Illustration don'ts
- Icon system: size scale, color on dark vs. light, container treatment
- Status icons, category icons, functional icons
- Icon don'ts

### 8. Component Stylings
- Must include: buttons (all variants), cards, inputs, navigation
- Each component must define: base state, hover, focus, active (if applicable), transition timing
- No static-only descriptions

### 9. Layout Principles
- Spacing scale (base unit + increments)
- Grid system and container widths
- Section spacing
- Whitespace philosophy

### 10. Depth & Elevation
- Named elevation levels
- Exact shadow values
- Usage rules per level

### 11. Do's and Don'ts
- Minimum 10 rules each (Do's and Don'ts)
- Must cover: color, typography, logo, photography, and illustration
- These are enforced rules, not suggestions

### 12. Responsive Behavior
- Breakpoints with specific widths
- Layout changes per breakpoint
- Typography scaling
- Component stacking logic

### 13. Agent Prompt Guide
- Named token reference for colors, typography, surfaces
- Example prompts for: hero sections, cards, buttons, layout blocks, logo placement, illustration characters, icon usage, photography overlays
- Always reference semantic tokens — never vague terms like "blue" or "dark"

---

## preview.html and preview-dark.html Requirements

Each preview file must:
- Be fully self-contained — no external CSS or JS (web font `@import` is permitted)
- Accurately reflect every token defined in DESIGN.md
- Include all of: color palette swatches, typography scale, button variants, card examples, form elements, spacing system, border radius scale, elevation system
- Include: Logo section, Illustration Colors section, Icon System section
- Be responsive across mobile and desktop
- Show clear visual hierarchy

**Light mode** (`preview.html`): Light surface background, PI Blue and Pink as accents. Logo displayed on white and on a Sky Blue chip. Icon system on Light Gray containers.

**Dark mode** (`preview-dark.html`): Dark navy page background with graph paper grid overlay. This is the signature PI surface — it must feel unmistakably like the real brand. Logo displayed on Midnight Navy. Icon system on Ink Blue containers.

**Logo section in both files**: Show the horizontal lockup via the SVG file path. Show a mark-only placeholder using CSS geometry (shield shape). Label all logo color values including the flagged off-palette values `#252e73` and `#b8deff`.

**Illustration Colors section in both files**: Color chips for the character illustration palette: Sky Blue (`#2398FF`), Magenta Pink (`#F80590`), Lavender Purple (`#8759F2`), Aqua Blue (`#0EBFE5`), Seafoam Green (`#2AEAA7`). Labeled "Illustration palette".

**Icon System section in both files**: Grid of representative icons using Unicode symbols or simple CSS shapes. Sizes: 16px, 20px, 24px, 32px. On light: Sky Blue icons on Light Gray containers. On dark: Sky Blue icons on Ink Blue containers.

**Restrictions:**
- No emojis or icons in navigation
- No Do's and Don'ts section
- No external dependencies beyond web fonts

---

## README.md Requirements

Include:
- What this design system is based on
- What it is used for
- File structure explanation
- Notes about the expanded 13-section DESIGN.md and the new sections
- Explanation of the two logo SVG colors (`#252e73` and `#b8deff`) that fall outside the CSV palette and why they exist
- Limitations (custom fonts, asset dependencies, what is not covered)
- **Timeline & Roadmap section** — see rule below

### Timeline & Roadmap Rule

The README must always contain a Timeline & Roadmap section. This section is the living record of how the PI design system has evolved and where it is going.

**When regenerating the README:**
1. Read the existing README before writing the new one
2. Copy the entire Timeline & Roadmap section from the old README into the new one exactly as-is
3. Then append any new events or roadmap updates that reflect work completed in the current session
4. Never delete or rewrite past timeline entries — only append

The Timeline & Roadmap section must contain two subsections:

**Completed** — a table of dated events, most recent last:

| Date | Event |
|------|-------|
| Summer 2025 | Current version of PI course design created |
| Late 2025 | Figma design guide created |
| April 2026 | First version of the code-based PI design system created (this repository) |

**Roadmap** — a prioritised table of upcoming work:

| Priority | Goal | Description |
|----------|------|-------------|
| Next | Complete Brand Foundation | ... |
| Next | Build out modules/ | ... |
| Medium | Replace Figma design guide with a CI/CD mini site | ... |
| Long-term | Automated asset generation | ... |
| Long-term | Automated asset processing pipeline | Person drops input file into shared folder (GitHub, Dropbox, Drive) → GitHub Action triggers → routes to correct module based on folder path or file metadata → Claude reads specs and processes input → output file saved and PR/review link sent to person → they approve or request changes |

When a roadmap item is completed, move it to the Completed table with the date it was done.

---

## Validation Checklist

Before finalising, verify every item:

- [ ] All 13 DESIGN.md sections are present and complete
- [ ] Every color in every file traces back to a row in the CSV
- [ ] No hex value appears in any output that is not in the CSV, except `#252e73` and `#b8deff` in the logo section only
- [ ] Every color entry includes: name (verbatim from CSV), hex, role, usage context
- [ ] Logo section documents all three variants, color modes, clear space, minimum size, and misuse rules
- [ ] Logo SVG off-palette values are explicitly flagged in DESIGN.md and README.md
- [ ] Photography section covers subject categories, style rules, overlay treatments, and don'ts
- [ ] Illustration section covers character rules, equipment icons, color enforcement, and don'ts
- [ ] Icon section covers size scale, color on dark and light, container treatment, and icon types
- [ ] Typography table covers the full hierarchy
- [ ] All components include hover, focus, and active states
- [ ] Both preview files include: Logo section, Illustration Colors section, Icon System section
- [ ] Both preview files render correctly and reflect DESIGN.md
- [ ] Dark preview uses the graph paper grid texture on navy
- [ ] Light and dark previews are visually consistent with each other
- [ ] Do's section has at least 10 items covering color, type, logo, photography, and illustration
- [ ] Don'ts section has at least 10 items covering color, type, logo, photography, and illustration
- [ ] Agent Prompt Guide includes examples for logo, illustration, icons, and photography
- [ ] README is complete and references the off-palette logo values
- [ ] No generic atmosphere language ("clean", "modern", "minimal") anywhere

---

## /note Command

When the user runs `/note`, Claude must:

1. Summarise the current conversation — decisions made, files changed, context discussed, anything worth preserving.
2. Determine the filename: `notes/YYYY-MM-DD.md` using today's date.
3. **If the file does not exist** — create it with the following structure:

```
# Notes — YYYY-MM-DD

## [Timestamp or session title]

[Summary of conversation]
```

4. **If the file already exists** — append a new section to the bottom of the file:

```

## [Timestamp or session title]

[Summary of conversation]
```

Do not overwrite existing content. Always append when the file exists.

---

## Final Rule

If the system reads like a generic UI kit, it has failed.

It must function as a coherent, distinctive design language that encodes intent — not just appearance.
