# the-bench
**Date:** 2026-04-17

---

#### Discussion Topics

Produced a full webinar script and design brief for introducing The Bench to colleagues. Materials cover the problem it solves, core concepts, commands, folder structure, onboarding steps, and prior art framing.

Also updated `actions/on-demand/actions-dashboard/server.py` — fixed all `run` command paths from `~/ZV-Bench/` to `~/dev/dev-ZV/ZV-Bench/` and corrected the `GITHUB` URL from `zzhenia/research` to `zzhenia/ZV-Bench`.

---

## Webinar Script

### Slide 1 — Title

**Speaker notes:**
> "Today I want to walk you through something I've been building over the last few months — a personal workspace called **The Bench**. It's not a product or a SaaS tool. It's a framework that lives in a GitHub repo on your laptop, and by the end of this I'll show you exactly how to get your own copy running."

---

### Slide 2 — The Problem

**Headline:** *You have the tools. You don't have a registry.*

**Speaker notes:**
> "Most of us already have all the pieces: Jira for tickets, Asana for tasks, a note-taking app, some scripts lying around, maybe an AI chat open in another tab. The problem isn't the tools — it's that there's no single source of truth connecting them. You copy-paste ticket IDs, you bookmark the same pages repeatedly, and automation never gets built because you can't even answer the question 'what project maps to what ticket in what system?'"
>
> "The Bench solves exactly that. It's a personal registry plus an execution layer."

---

### Slide 3 — What The Bench Is

**Headline:** *One repo. Persistent AI context. Everything connected.*

**Bullet points on slide:**
- Claude Code (terminal AI with memory across sessions)
- VS Code (editing)
- Obsidian (note linking and search)
- GitHub (version control + private backup)

**Speaker notes:**
> "The Bench is a folder. A very opinionated folder. It combines four tools you probably already have: Claude Code as the brain, VS Code for editing, Obsidian for visual search and linking, and a private GitHub repo for version control. Every session, every decision, every script — versioned and findable."

---

### Slide 4 — The Two-Part Structure

**Headline:** *Actions and Convos*

**Visual:** Two-column split

**Left — Actions:**
- Repeatable tasks Claude executes
- Each has `instructions.md` + `assets/`
- **On-demand:** run manually
- **Recurring:** scheduled (launchd/cron)

**Right — Convos:**
- Ongoing research topics
- Persistent context across sessions
- Each session → one dated note (`YYMMDD-short-description.md`)

**Speaker notes:**
> "The whole workspace splits into two buckets. **Actions** are repeatable tasks — meeting minutes, weekly check-ins, ticket syncing. You drop files into `assets/`, tell Claude to follow `instructions.md`, done. **Convos** are ongoing topics — a research thread, a project you're tracking, a decision you're working through. Claude reads the last few notes at the start of every session, so it has full context without you having to re-explain anything."

---

### Slide 5 — The Commands

**Headline:** *Four commands do most of the work*

**Table on slide:**

| Command | What it does |
|---|---|
| `/note` | Writes a session note; posts to the linked ticket |
| `/push` | Commits everything + runs `/note` |
| `/status` | Snapshot of all scheduled automations |
| `/ai` | Processes inline `@ai` annotations in any file |

**Speaker notes:**
> "There are four slash commands baked into the template. `/note` is the one you'll use most — at the end of any session, it asks Claude to write a dated summary into the right folder, and if that folder is linked to a Jira or Asana ticket, it posts the note there automatically. `/push` chains that into a git commit and push. `/status` gives you a live view of your scheduled jobs. `/ai` is for inline AI editing — tag any line with `@ai` and a prompt, run the command, done."

---

### Slide 6 — Bench Index

**Headline:** *`bench-index.csv` — the registry*

**Visual:** Screenshot or mock of the CSV with columns: `slug`, `type`, `convo_folder`, `action_folder`, `jira`, `asana`

**Speaker notes:**
> "The connective tissue is `bench-index.csv`. Every action and convo gets a row. Every row can have a Jira key and an Asana task GID. When you run `/note` or `/push`, Claude looks up the slug, finds the ticket, and posts the note as a comment automatically. If there's no ticket yet, it searches Jira and Asana for you, and if it still can't find one, it offers to create it."

---

### Slide 7 — Folder Structure

**Headline:** *The full layout*

**Visual:** Tree diagram (code block style)

```
your-bench/
├── master-instructions.md
├── bench-index.csv
├── config/
│   └── keys.env.template
├── actions/
│   ├── dashboard/
│   ├── on-demand/
│   └── recurring/
├── convos/
│   └── Templates/
└── .claude/
    ├── commands/
    └── skills/
```

**Speaker notes:**
> "Here's what you get when you clone the template. `master-instructions.md` is Claude's operating guide — it reads this at the start of every session. `config/` holds your API keys (gitignored, never committed). `actions/` has two sub-folders: on-demand for manual tasks, recurring for scheduled ones. `convos/` is where all your topic threads live. And `.claude/` has the commands and skills wired up and ready to go."

---

### Slide 8 — Getting Started

**Headline:** *Five steps to your own bench*

**Numbered list:**
1. Get added as a collaborator on `zzhenia/bench-template`
2. Click "Use this template" on GitHub — name it (e.g. `my-bench`)
3. Clone locally and run `./setup.sh`
4. Fill in `config/keys.env` with your API keys
5. `claude .` — you're in

**Speaker notes:**
> "The template is a private GitHub repo. I add you as a collaborator, you click 'Use this template', give it a name, clone it, run one setup script. That's it. Your bench is independent from mine — I can push updates to the template but they won't overwrite yours. You pull what you want."

---

### Slide 9 — How It Fits (Prior Art)

**Headline:** *This is platform engineering for an org of one*

**Bullet points:**
- Notion Life OS → same instinct, no automation layer
- GitHub's "Scripts to Rule Them All" → same pattern, applied personally
- Dotfiles repos → version control without cross-API glue
- n8n/Activepieces → visual, but no git history, no Claude

**Speaker notes:**
> "There are a lot of adjacent frameworks. Notion Life OS, dotfiles repos, self-hosted automation tools. They all solve a piece of this. The gap they all share is the registry problem — no single source of truth for what maps to what. And none of them have an AI that reads your session history and picks up exactly where you left off."

---

### Slide 10 — Live Demo / Q&A

**Headline:** *Let's look at it*

**Speaker notes:**
> "I'll share my screen and walk through a real session — starting Claude, switching convo context with `@name`, running `/note` at the end, and watching it post to Jira. Then open floor for questions."

---

## Design Brief for Webinar Agent

### Overall tone and aesthetic
- Clean, technical, minimal. Think internal engineering presentation, not marketing deck.
- Dark background (slate `#1e2127` or similar) with light text. Code blocks should look like a real terminal.
- Accent color: amber/gold (`#f0a500`) for highlights, command names, and key terms.
- Font: monospace for all code, labels, command names (`JetBrains Mono` or `Fira Code`). Clean sans-serif for body (`Inter` or `IBM Plex Sans`).

### Slide layouts

**Slide 1 (Title):** Full-bleed dark background. Large centered title: "The Bench". Subtitle: "A personal knowledge and automation workspace". Bottom-right: presenter name + date. Optional: faint grid or terminal cursor blink animation.

**Slide 2 (Problem):** Headline + body text only. Key phrase "registry problem" bold or in accent color.

**Slide 3 (What it is):** Four tool logos in 2×2 grid (Claude, VS Code, Obsidian, GitHub) — monochrome/desaturated. Short label each.

**Slide 4 (Two-part structure):** Strict two-column split with thin dividing line. Section headers in accent color, bullets below.

**Slide 5 (Commands):** Four-row table. Command names in monospace amber. Descriptions in regular weight.

**Slide 6 (Bench Index):** Left half: CSV rendered as clean HTML table, column headers in accent color. Right half: two-sentence explanation.

**Slide 7 (Folder structure):** Full-slide terminal/code block. Inline comments in muted gray to the right of key lines.

**Slide 8 (Getting started):** Numbered steps, large and scannable. Step numbers in accent color circles. Steps 3 and 5 in monospace.

**Slide 9 (Prior art):** Bullet list — framework name bold, one-line contrast in regular weight. Last bullet ("The gap") slightly larger or in accent color.

**Slide 10 (Demo/Q&A):** Minimal — just headline and a centered terminal prompt graphic or blinking cursor.

### Slide dimensions
- 16:9 widescreen (1920×1080 or 1280×720)

### Slide count
- 10 slides total as scripted above.

### Deliverable format
- PowerPoint (`.pptx`) or Google Slides export preferred. If Figma/Canva, export as PDF + editable source.

---

#### References

- `convos/the-bench/` — all bench session notes
- `master-instructions.md` — operating guide (source material for slides 3–7)
- `https://github.com/zzhenia/bench-template` — template repo (source for slides 7–8)
- `actions/on-demand/actions-dashboard/server.py` — paths updated this session
