# Notes — 2026-04-07

## Session — First Release, GitHub Pages Mini Site, Claude Code Skill

---

### Context

Planning the v1 release of the PI design system so that team members can start using it. The repo already existed at `github.com/Pilot-Institute/pi-design-system` with the core design system files complete (`DESIGN.md`, both previews, `README.md`, `segments/`, `modules/`).

---

### Key decisions made

#### 1. Distribution architecture — thin skill, central source of truth

Decided against duplicating design system content into multiple SKILL.md copies. The correct architecture is:

- **One source of truth**: this GitHub repo
- **Thin SKILL.md bootstrap**: the installed skill file contains no design system content — it fetches the latest Instructions.md and DESIGN.md from GitHub raw URLs at invocation time
- **Implication for releases**: pushing to `main` is the release. Users get updates automatically on next `/pi-design` invocation with no redistribution required

This is especially important because v2 (modules release) is planned for this week or early next week.

#### 2. Claude Code skill created

File: `.claude/skills/pi-design-system/SKILL.md`

- Slash command: `/pi-design`
- Fetches `Instructions.md` from raw GitHub on invocation
- Handles segment selection (airplanes default) and module routing
- Accompanied by `SETUP.md` with curl-based install instructions

Users install by copying the entire `pi-design-system/` subfolder to `~/.claude/skills/`.

#### 3. GitHub Pages mini site

- Folder: `docs/` (required name for GitHub Pages branch-based deploy)
- File: `docs/index.html` — merged light + dark preview into a single page with a CSS/JS light/dark mode toggle (dark is default)
- Toggle: fixed bottom-right, pill shape, sun/moon icon, localStorage persistence
- Assets copied to `docs/assets/` (logos + all reference images)
- GitHub Pages enabled in repo settings: branch `main`, folder `/docs`
- Live URL: `https://pilot-institute.github.io/pi-design-system/`
- Custom domain option: `design.pilotinstitute.com` is possible via DNS CNAME — requires someone with domain access to add the record, then enter it in repo Settings → Pages → Custom domain

#### 4. Caution: repo is private, site is public

GitHub showed a warning that the repo is private but the Pages site will be publicly accessible. Team should be aware.

---

### File structure changes this session

```
.claude/skills/pi-design-system/
├── SKILL.md      ← installable Claude Code skill
└── SETUP.md      ← install instructions

docs/
├── index.html    ← merged light/dark preview with toggle
└── assets/       ← PI_logo_hor-dark.svg, PI_logo_hor-light.svg, all Design-guide-*.png, Lead-magnet-*.jpg
```

Removed: `design-system/preview.html` and `design-system/preview-dark.html` are now superseded by `docs/index.html` (though the old files still exist in `design-system/` — pending cleanup).

---

### Pending / next steps

- **v2 release — modules**: Build out all `modules/` spec files this week or early next week. This is the primary next task. Once pushed to `main`, all skill users get it automatically.
- **Delete old preview files**: `design-system/preview.html` and `design-system/preview-dark.html` can be removed once the team confirms `docs/index.html` is the canonical reference.
- **Custom domain (optional)**: Enter `design.pilotinstitute.com` in repo Settings → Pages if DNS CNAME is set up.
- **Brand Foundation (Section 2)**: Still a placeholder — Zhenia to supply vision, mission, core values, key audiences.

---

## Session — Continued: Skill testing, cleanup, architecture decisions

---

### Skill installation testing

Walked through the full install flow. Issues found and resolved:

1. **Backslash line-break in curl command** — when copied from chat, the `\` continuation character caused `curl: (3) URL malformed`. Fixed by writing the curl command as a single line in SETUP.md.
2. **Wrong URL in SETUP.md** — pointed to the old flat path (`.claude/skills/pi-design-system.md`) after we had moved the file into a subfolder. Fixed to `.claude/skills/pi-design-system/SKILL.md`.
3. **Repo was private** — raw GitHub URLs return 404 for private repos. Repo was made public to allow unauthenticated skill installs.
4. **Broken skill file installed** — curl had saved a "404: Not Found" response as the SKILL.md. Re-running the corrected curl command after making the repo public resolved it. Confirmed working: curl downloaded 3273 bytes (the real skill file).

**Install command (final, working):**
```bash
mkdir -p ~/.claude/skills/pi-design-system
curl -o ~/.claude/skills/pi-design-system/SKILL.md https://raw.githubusercontent.com/Pilot-Institute/pi-design-system/main/.claude/skills/pi-design-system/SKILL.md
```

---

### Skill test — troubleshooting-guide.html

Tested `/pi-design` on `/Users/zheniavasiliev/Downloads/troubleshooting-guide.html`. The skill correctly identified and fixed all token violations:

| Violation | Before | After |
|-----------|--------|-------|
| Font | `Lexend` (not a PI font) | `Arial` body, `Eina/Arial` display |
| Page background | Light gray (light-first) | Midnight Navy + graph paper grid |
| Cards | White | Ink Blue with Steel Blue border |
| Off-palette colors | `#293A4E`, `#1a1f3d`, `#4a5568`, `#8896a6`, `#b0b8c4`, `#0b7ad8` | Replaced with PI palette tokens |
| Warning callout border | Magenta Pink (wrong semantic) | Tomato Red `#FF464A` |
| Quick link icons | Emoji | Inline SVG |

**Key finding**: the skill's raw GitHub fetch fails for private repos. Now resolved (repo is public).

---

### Architecture decisions

#### Color sync risk in docs/index.html
Colors in `docs/index.html` are hardcoded CSS variables — a potential sync issue if the CSV updates without regenerating the HTML. Decision: acceptable for now, managed by process (regenerate HTML when CSV changes). Long-term fix is the CI/CD mini site roadmap item. A note should be added to `Instructions.md` flagging `docs/index.html` as a generated artifact.

#### CSV location stays in reference/
`reference/PI-Colour-Palette.csv` stays in `reference/` — it is a source input, not a generated output. Moving it to `design-system/` would blur source vs. output. The folder distinction is intentional:
- `reference/` — raw source inputs (CSV, images, design guide exports)
- `design-system/` — generated outputs (DESIGN.md, README.md)
- `docs/` — generated outputs (index.html, assets)

---

### Cleanup completed this session

- Deleted `design-system/preview.html` and `design-system/preview-dark.html` — superseded by `docs/index.html`
- Deleted 13 unused image files from `docs/assets/` (Design-guide-*.png, Lead-magnet-*.jpg) — never referenced by index.html, were copies of reference/img/
- `docs/assets/` now contains only `PI_logo_hor-dark.svg` and `PI_logo_hor-light.svg` (both used by index.html)
- Fixed `design-system/README.md` file structure section to reflect current state
- Updated SETUP.md visual reference section to point to GitHub Pages URL instead of deleted preview files

---

### Updated pending / next steps

- **Add `docs/index.html` to Instructions.md** as a generated artifact that must be regenerated when the CSV changes
- **v2 release — modules**: primary next task
- **Custom domain**: `design.pilotinstitute.com` via DNS CNAME (optional)
- **Brand Foundation (Section 2)**: Zhenia to supply

---

## Session — Docs Site Polish + Font Embedding + Skill Grid Rule

---

### Background grid pattern changes

Removed the full-page background grid (`body::before`) that covered the entire site. Grid now appears only in:
- **Hero section** (`.hero::before`) — fades from opaque at top to transparent at bottom
- **Gobold impact block** (`.impact-block::before`) — fades in/out top and bottom

Initially also accidentally removed hero and impact-block grids; restored them in a follow-up commit.

**Impact block full-width fix**: `.impact-block` sits inside `.container` (max-width 1140px), so `inset: 0` was clipping the grid. Fixed with `left: 50%; width: 100vw; transform: translateX(-50%)` to break out of the container.

---

### Hero title typography

Updated `.hero-title` to match user's DevTools test values:
- `font-size: 71px`
- `font-weight: 700` (updated from 600 in a later pass)
- `line-height: 0.9`
- `letter-spacing: 2px`

Note: Eina only has four weights — Light (300), Regular (400), Semibold (600), Bold (700). No 800/ExtraBold exists in the font family.

---

### Web font embedding (Eina + Gobold)

Fonts were only referenced by name — worked on machines with Eina installed, failed elsewhere (showing "Aurel"/system font fallback).

**Fix**: Extracted fonts from `Eina.ttc` using fonttools/Python, converted to `.woff2`, hosted in `docs/fonts/`, added `@font-face` declarations.

Font files added:
| File | Weight |
|------|--------|
| `Eina-Light.woff2` | 300 |
| `Eina-Regular.woff2` | 400 |
| `Eina-Semibold.woff2` | 500–600 |
| `Eina-Bold.woff2` | 700 |
| `Gobold-Bold.woff2` | 700 |

Source: `Eina.ttc` (indices 5, 6, 4, 2) + `gobold/Gobold Bold.otf`. Intermediate TTF/OTF files removed after conversion. The Eina01–04 TTF variant set the user also has are optical-size variants with the same weight range — not needed.

Tool used: `pip install fonttools brotli` → `font.flavor = 'woff2'; font.save(...)`.

---

### DESIGN.md — HTML grid implementation rule

The DESIGN.md already said the grid was "never optional on dark surfaces" but gave no HTML implementation guidance. Added:

1. **New section "HTML Implementation — Graph Paper Grid"** in the token table area — exact copy-paste CSS snippet including the full-width breakout variant for elements inside containers
2. **Updated Iteration Guide rule #6** — now explicitly states "implement as `::before` on the top section" and "must appear at least once in every HTML page output"

Motivation: a button spec page generated by the skill outside this repo was missing the grid because the agent knew the rule conceptually but had no implementation code to follow.

---

### Robots meta tag

Added `<meta name="robots" content="noindex, nofollow">` to `docs/index.html` per Johann's Slack request. `nocrawl` is not a standard directive — `nofollow` is the correct equivalent.
