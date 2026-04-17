# Note Command Update
**Date:** 260417

#### Discussion Topics

Two rounds of updates to the `/note` command:
1. Routing fix — non-bench repos (no `bench-index.csv`) were incorrectly prompted for `convos/` folders and ticket posting.
2. Naming convention sync — aligned with ZV-Bench standard: `YYMMDD-short-description.md` per session, replacing the old `YYYY-MM-DD.md` append-per-day approach. Adopted ZV-Bench template structure.

#### Key Decisions

- Non-bench repos use `notes/YYMMDD-short-description.md` — one file per session, no ticket posting.
- Global command (`~/.claude/commands/note.md`) detects `bench-index.csv` to route between Path A (bench) and Path B (simple notes).
- Template structure adopted from ZV-Bench: Discussion Topics / Key Decisions / Actions / References / Open Questions.
- `NOTE-SYSTEM.md` in root dev folder is the canonical spec for the simple system.

#### Actions

| Item | Owner | Notes |
|------|-------|-------|
| Rename any old bare-date note files in this repo | Zhenia | `2026-04-03.md` and `260407-first-release.md` still use old naming |

#### References

- `~/.claude/commands/note.md` — global note command (Path A / Path B routing)
- `/Users/zheniavasiliev/dev/NOTE-SYSTEM.md` — canonical spec for simple notes/ system
- `.claude/commands/note.md` (this repo) — local command, non-bench path
- `/Users/zheniavasiliev/dev/dev-ZV/ZV-Bench/.claude/commands/note.md` — source of naming convention

#### Open Questions

- Should older notes (`2026-04-03.md`, `260407-first-release.md`) be migrated to the new naming convention?
