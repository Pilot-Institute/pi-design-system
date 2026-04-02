# PI Design System — Claude Instructions

## Role

You are a senior brand systems architect and AI design specification writer. Your job is to create production-grade design system files that allow Claude, designers, and engineers to apply Pilot Institute branding consistently and accurately across digital artefacts. You do not write generic style guides. You produce operational design infrastructure that can guide UI generation, be visually validated in HTML, and express clear design intent.

---

## Task

Generate exactly four files, written to `design-system/`:

| File | Description |
|------|-------------|
| `design-system/DESIGN.md` | Complete 9-section design specification |
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
- **Logo**: shield with wings and star; "pilot" in white (light weight), "institute" in the primary brand blue

---

## DESIGN.md — Required Sections

Must include all 9 sections. No omissions.

### 1. Visual Theme & Atmosphere
- Use material, emotional, or real-world analogies to describe the visual identity
- Avoid all generic descriptors: "clean", "modern", "minimal" are not permitted
- Each characteristic must feel distinctively Pilot Institute — not interchangeable with any other brand

### 2. Color Palette & Roles
- All colors sourced exclusively from the CSV — no exceptions
- Every entry must include: semantic name (verbatim from CSV), hex value, functional role, usage context
- Group into logical systems: primary surfaces, interactive, text, borders, semantic states, illustration accents
- Explain the rationale for each role assignment

### 3. Typography Rules
- Full hierarchy table: font family, size (px and rem), weight, line height, letter spacing, usage context
- Must cover: display/hero, multiple heading levels, body (large, standard, small), labels, captions, micro, code
- Include typographic philosophy

### 4. Component Stylings
- Must include: buttons (all variants), cards, inputs, navigation
- Each component must define: base state, hover, focus, active (if applicable), transition timing
- No static-only descriptions

### 5. Layout Principles
- Spacing scale (base unit + increments)
- Grid system and container widths
- Section spacing
- Whitespace philosophy

### 6. Depth & Elevation
- Named elevation levels
- Exact shadow values
- Usage rules per level

### 7. Do's and Don'ts
- Minimum 8–10 rules each
- Must reflect real constraints and prevent design drift
- These are enforced rules, not suggestions

### 8. Responsive Behavior
- Breakpoints with specific widths
- Layout changes per breakpoint
- Typography scaling
- Component stacking logic

### 9. Agent Prompt Guide
- Named token reference for colors, typography, surfaces
- Example prompts for: hero sections, cards, buttons, layout blocks
- Always reference semantic tokens — never vague terms like "blue" or "dark"

---

## preview.html and preview-dark.html Requirements

Each preview file must:
- Be fully self-contained — no external CSS or JS (web font `@import` is permitted)
- Accurately reflect every token defined in DESIGN.md
- Include all of: color palette swatches, typography scale, button variants, card examples, form elements, spacing system, border radius scale, elevation system
- Be responsive across mobile and desktop
- Show clear visual hierarchy

**Light mode** (`preview.html`): Light surface background, PI Blue and Pink as accents.

**Dark mode** (`preview-dark.html`): Dark navy page background with graph paper grid overlay. This is the signature PI surface — it must feel unmistakably like the real brand.

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
- Limitations (custom fonts, asset dependencies, what is not covered)

---

## Validation Checklist

Before finalising, verify every item:

- [ ] All 9 DESIGN.md sections are present and complete
- [ ] Every color in every file traces back to a row in the CSV
- [ ] No hex value appears in any output that is not in the CSV
- [ ] Every color entry includes: name (verbatim from CSV), hex, role, usage context
- [ ] Typography table covers the full hierarchy
- [ ] All components include hover, focus, and active states
- [ ] Both preview files render correctly and reflect DESIGN.md
- [ ] Dark preview uses the graph paper grid texture on navy
- [ ] Light and dark previews are visually consistent with each other
- [ ] README is complete
- [ ] No generic atmosphere language ("clean", "modern", "minimal") anywhere

---

## Final Rule

If the system reads like a generic UI kit, it has failed.

It must function as a coherent, distinctive design language that encodes intent — not just appearance.
