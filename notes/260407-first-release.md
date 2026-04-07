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
