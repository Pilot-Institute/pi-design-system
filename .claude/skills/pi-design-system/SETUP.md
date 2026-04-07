# PI Design System — Setup Guide

This guide explains how to install the PI design system as a Claude Code skill. Once installed, you can apply Pilot Institute branding in any project by running `/pi-design` followed by your request.

---

## Requirements

- [Claude Code](https://claude.ai/code) installed and running
- Internet access (the skill fetches the latest design system from GitHub at invocation time)

---

## Installation

**1. Create the skills directory (if it doesn't exist)**

```bash
mkdir -p ~/.claude/skills/pi-design-system
```

**2. Copy the skill file**

```bash
curl -o ~/.claude/skills/pi-design-system/SKILL.md https://raw.githubusercontent.com/Pilot-Institute/pi-design-system/main/.claude/skills/pi-design-system/SKILL.md
```

That's it. The skill is now available in every Claude Code session.

---

## Usage

In any project, open Claude Code and run:

```
/pi-design [your request]
```

**Examples:**

```
/pi-design create a YouTube thumbnail for the airplanes segment, topic: "How to Pass Your Part 107 Exam"
/pi-design design a lead magnet cover for the drones segment
/pi-design write the design spec for a landing page hero section, helicopters segment
/pi-design create an Instagram post for the flight attendant segment
```

**Processing an existing HTML file:**

```


```

Claude will read the file, fetch the PI design system, apply all corrections, and write the fixed HTML back. To keep the original untouched, specify a different output path:

```
/pi-design review and rewrite /path/to/file.html to be PI brand compliant. Save the corrected file to /path/to/file-v2.html
```

To also get a written summary of what was changed:

```
/pi-design review and rewrite /path/to/file.html to be PI brand compliant. Save the corrected file to the same path, and write a brief change summary to /path/to/changes.md
```

---

## How it works

The installed skill file is a thin bootstrap — it contains no design system content itself. Every time you invoke `/pi-design`, Claude fetches the current version of the design system directly from this GitHub repository and applies it to your request.

**This means:**
- You install the skill once and never update it
- Design system updates (new releases, new modules) are available automatically
- There is one source of truth: this repository

---

## Visual reference

The design system ships with a visual token catalog — a single page with a light/dark mode toggle:

**GitHub Pages (no setup required):**
https://pilot-institute.github.io/pi-design-system/

**Local file (if you have the repo cloned):**
`docs/index.html` — open in any browser

---

## Updating

Because the skill always fetches from `main`, you never need to update the installed skill file. New releases are live immediately after they are pushed to this repository.

---

## Troubleshooting

**`/pi-design` command not found**
Verify the skill file is at the correct path: `~/.claude/skills/pi-design-system/SKILL.md`

**Output doesn't look like Pilot Institute**
Make sure you specified a segment (airplanes, drones, helicopters, flight attendant). If omitted, the system defaults to Airplanes.

**Module not found**
Some modules are still being built out. If a module file is a stub or missing, the skill falls back to the base design specification in `DESIGN.md`.
