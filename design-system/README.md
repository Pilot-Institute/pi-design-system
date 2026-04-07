# Pilot Institute Design System

## What this is based on

This design system is derived from the official Pilot Institute Design Guide (260401), the PI Colour Palette, analysis of live Pilot Institute brand materials including course content, lead magnets, white papers, and website screencaptures, and inspection of the official logo SVG assets. It follows the DESIGN.md format established by Google Stitch and refined through Anthropic's brand system examples.

## What it is used for

This system is operational design infrastructure — not a style guide. It enables:

- **AI agents** (Claude, Cursor, Google Stitch) to generate consistent Pilot Institute UI without screenshots
- **Designers** to make brand-aligned decisions with precise token references
- **Engineers** to implement components that faithfully reflect the brand
- **Content creators** to apply correct typography, color, and layout rules across digital and print materials

The system covers digital interfaces (web, course UI, email) and editorial print outputs (study sheets, white papers, lead magnets). Output-specific extensions are maintained separately in `/modules`.

## File structure

```
design-system/
├── DESIGN.md     ← Complete 13-section design specification (primary reference)
└── README.md     ← This file

docs/
├── index.html    ← Visual token catalog with light/dark toggle (single source of truth)
└── assets/       ← Logo SVGs and reference images
```

Supporting source material lives in `reference/`:
```
reference/
├── PI-Colour-Palette.csv    ← Single source of truth for all color values
├── img/                     ← Design guide exports, real-world output samples, and logo SVG files
├── branding/                ← Established brand application rules (thumbnails, charts)
├── website/                 ← Website screencaptures (live design in context)
└── output-examples/         ← Benchmark-quality DESIGN.md examples (Claude, Apple)
```

## DESIGN.md — 13-Section Structure

The design specification covers all foundational and applied brand rules in 13 sections:

| Section | Title | Status |
|---------|-------|--------|
| 1 | Visual Theme & Atmosphere | Complete |
| 2 | Brand Foundation | Placeholder — requires brand team input |
| 3 | Logo System | Complete |
| 4 | Color Palette & Roles | Complete |
| 5 | Typography Rules | Complete |
| 6 | Photography | Complete |
| 7 | Illustration & Icons | Complete |
| 8 | Component Stylings | Complete |
| 9 | Layout Principles | Complete |
| 10 | Depth & Elevation | Complete |
| 11 | Do's and Don'ts | Complete — 12 rules each |
| 12 | Responsive Behavior | Complete |
| 13 | Agent Prompt Guide | Complete — includes logo, illustration, icon, and photography prompts |

**New sections since the previous 9-section version**:

- **Section 2 (Brand Foundation)**: Placeholder requiring the brand team to supply vision, mission, core values, and key audience profiles. A "known brand orientation" summary is included based on available reference material.
- **Section 3 (Logo System)**: Documents the shield mark anatomy, wordmark treatment, three variants (horizontal, mark-only, stacked), color modes, clear space rules, minimum sizes, and 8 misuse rules. Also documents the two off-palette SVG values (see below).
- **Section 6 (Photography)**: Covers the four photography categories, style rules for contrast and authenticity, specific overlay gradient treatments (course card, hero, lead magnet), and photography don'ts.
- **Section 7 (Illustration & Icons)**: Covers flat vector illustration style, character rules, the five-color illustration palette, equipment illustrations, infographic color usage, illustration don'ts, and the complete icon system (size scale, color rules, container treatment, aviation category icons, functional icons, status icons).

## Logo SVG colors outside the CSV palette

The official logo SVG files in `reference/img/` use two hex values that do not appear in `PI-Colour-Palette.csv`:

**`#252e73`** — the dark wordmark color used in `PI_logo_hor-dark.svg` (the logo variant for light backgrounds). This value predates the CSV color system. The closest CSV equivalent for reference purposes only is Electric Indigo (`#2E4292`), but they are not interchangeable. `#252e73` must not be used as a design token for any element outside the logo SVG files.

**`#b8deff`** — a light element used in certain logo variants. The closest CSV equivalent for reference purposes only is Baby Blue (`#81D1F4`), but they are not interchangeable. `#b8deff` must not be used as a design token for any element outside the logo SVG files.

These values are pre-existing logo asset values locked into the official SVG artwork. They exist because the logo was created before the current CSV-based token system was established. The SVG files are the authoritative source for logo reproduction — do not attempt to recreate the logo using CSV colors as substitutes. When placing the logo, always reference the SVG file directly.

These values are documented in DESIGN.md Section 3 and in both preview HTML files. They are not in the token system and must not propagate outside the logo context.

## Timeline & Roadmap

This section is part of the living record of the PI design system. When the design system is regenerated, carry this section forward into the new README and append any new events.

### Completed

| Date | Event |
|------|-------|
| Summer 2025 | Current version of PI course design created — established the visual language used across all course UI, thumbnails, and course materials |
| Late 2025 | Figma design guide created — first consolidated reference for PI brand, covering colour, typeface, logo, illustration, photography, and visual devices |
| April 2026 | First version of the code-based PI design system created (this repository) — translates the Figma design guide into operational design infrastructure: a structured file system with token-based specifications, automated colour palette sync from Google Sheets, and segment/module architecture |

### Roadmap

| Priority | Goal | Description |
|----------|------|-------------|
| Next | Complete Brand Foundation | Supply vision, mission, core values, and key audience profiles to complete Section 2 of DESIGN.md |
| Next | Build out modules/ | Create format-specific specification files for all output types: video, graphics (social media, editorial, events), ads, 2D animation, 3D animation, troubleshooting guides |
| Medium | Replace Figma design guide with a CI/CD mini site | Migrate the design guide from a static Figma file to a generated website that contains all design specifications, visual token previews, and usage examples — automatically updated whenever the design system files change. The site would serve as the single source of truth for all team members, replacing the current Figma file with a format that is version-controlled, always current, and accessible without a Figma licence |
| Long-term | Automated asset generation | Integrate the design system with asset production pipelines so that design tokens directly drive output generation (thumbnails, social posts, course cards) without manual recreation |
| Long-term | Automated asset processing pipeline | A person drops a raw input file into a shared folder (GitHub, Dropbox, or Drive). A GitHub Action triggers, routes the file to the correct module based on folder path or file metadata, Claude reads the relevant design spec and processes the input, the output file is saved and a PR or review link is sent to the person, and they approve or request changes. This closes the loop between raw assets and brand-compliant outputs without requiring manual tool access. |

---

## How to regenerate

1. Open this repo in Claude Code
2. Make any changes to `reference/PI-Colour-Palette.csv` (for color updates) or source images
3. Run: `Generate the PI design system per Instructions.md`
4. All four files in `design-system/` will be regenerated

When the colour palette CSV is updated, all output files will reflect the changes on next generation — no edits to `Instructions.md` are required.

## Limitations

**Custom fonts**: Eina and Gobold are licensed typefaces. The preview HTML files reference them via CSS font-family but will fall back to Arial if the fonts are not installed locally or embedded as web fonts. To see accurate typography rendering, add the font files to the project and update the `@font-face` declarations in the preview files. Do not substitute Montserrat, Futura, or other geometric fonts for Eina — they alter the brand's proportions.

**Brand Foundation incomplete**: Section 2 of DESIGN.md is a placeholder. Vision, mission, core values, and key audience profiles must be provided by the brand team. This section cannot be derived from visual reference material alone.

**Photography and illustration assets**: The design system documents rules for photography and illustration but does not include the actual photography library or the flat vector illustration library. Course cards and hero sections reference photography as a layer — actual images must be supplied separately.

**Logo SVG files**: The design system references logo SVG files at `../reference/img/PI_logo_hor-dark.svg` and `../reference/img/PI_logo_hor-light.svg`. If these files are missing or renamed, the logo section of both preview files will show broken images. The CSS shield mark placeholder will remain as a fallback indicator.

**Modules not included**: Output-specific extensions (video, organic social, blog, infographic, course, webinar, newsletter, print) are handled separately in `/modules` and are not part of this core system.

**Website PDF screencaptures**: The `reference/website/` PDFs require `poppler-utils` to render. Install via `brew install poppler` to enable future reads of those files.
