# Pilot Institute Design System

## What this is based on

This design system is derived from the official Pilot Institute Design Guide (260401), the PI Colour Palette, and analysis of live Pilot Institute brand materials including course content, lead magnets, white papers, and website screencaptures. It follows the DESIGN.md format established by Google Stitch and refined through Anthropic's brand system examples.

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
├── DESIGN.md          ← Complete 9-section design specification (primary reference)
├── preview.html       ← Light mode visual catalog — open in browser to validate tokens
├── preview-dark.html  ← Dark mode visual catalog — the primary PI surface
└── README.md          ← This file
```

Supporting source material lives in `reference/`:
```
reference/
├── PI-Colour-Palette.csv    ← Single source of truth for all color values
├── img/                     ← Design guide exports and real-world output samples
├── branding/                ← Established brand application rules (thumbnails, charts)
├── website/                 ← Website screencaptures (live design in context)
└── output-examples/         ← Benchmark-quality DESIGN.md examples (Claude, Apple)
```

## How to regenerate

1. Open this repo in Claude Code
2. Make any changes to `reference/PI-Colour-Palette.csv` (for color updates) or source images
3. Run: `Generate the PI design system per CLAUDE.md`
4. All four files in `design-system/` will be regenerated

When the colour palette CSV is updated, all output files will reflect the changes on next generation — no edits to `CLAUDE.md` are required.

## Limitations

**Custom fonts**: Eina and Gobold are licensed typefaces. The preview HTML files reference them via CSS font-family but will fall back to Arial if the fonts are not installed locally or embedded as web fonts. To see accurate typography rendering, add the font files to the project and update the `@font-face` declarations in the preview files.

**Photography and illustration**: The design system does not include photography assets or the flat vector illustration library. Course cards and hero sections reference photography as a layer — actual images must be supplied separately.

**Modules not included**: Output-specific extensions (video, organic social, blog, infographic, course, webinar, newsletter, print) are handled separately in `/modules` and are not part of this core system.

**Color derivation**: Two colors in the source palette (`#050845` used in earlier chart templates, `#252e73` used in earlier thumbnail prompts) do not appear in `PI-Colour-Palette.csv`. Per the CSV-as-source-of-truth rule, they are not included in this system. The closest equivalents from the CSV are `Midnight Navy (#0D0F20)` and `Slate Blue (#212353)`. If these values should be canonical, add them to the CSV and regenerate.

**Website PDF screencaptures**: The `reference/website/` PDFs require `poppler-utils` to render. Install via `brew install poppler` to enable future reads of those files.
