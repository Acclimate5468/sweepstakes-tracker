# Current Status — Sweepstakes Tracker

_Snapshot of where the project stands and what to do next._

## Repo state (live git values)
- **Branch:** `main` tracking `origin/main`
- **Sync:** 0 ahead / 0 behind — clean and synced with `origin/main`
- **Working tree at snapshot time:** clean (no uncommitted changes)
- **Last commit:** `e954bb5` — "Add deadline badges, auto-expire, rules
  checklist, dup detection, installable icon" (2026-06-02)
- **Remote:** `origin` → `github.com/Acclimate5468/sweepstakes-tracker` (**public**)

## App type
Single-file, offline-first browser app: **`sweepstakes.html`** (inline
HTML/CSS/JS). No install, no server, no build system, no dependencies, no test
framework. Data persists in browser `localStorage`; backups via in-app
JSON/CSV Export/Import.

## What is implemented
- Six-step manual workflow: Discovery → Rules review → Risk review → Score →
  Decide → Track.
- Tabs: 🏁 Home, 📋 Tracker, 🔍 Review, 📝 Log, ⚙️ More.
- Scoring across seven factors with strict disqualifying overrides
  (Pursue / Maybe / Skip / Research more).
- Entry tracking with next-eligible-date computation (daily/weekly/monthly/
  one-time) and warnings for too-early, over-limit, repeat one-time, and
  past-deadline entries.
- Deadline badges, auto-expire, rules checklist, duplicate detection,
  installable icon (per last commit).
- JSON/CSV export, import, reset, and a "Load Liquid Death example" loader.

## What is deferred
Per the README's stated direction, automation is **deliberately deferred**
until the manual workflow proves useful and safe — and even then limited to
low-risk reminders, **never** auto-entry. Deferred items include:
- Reminders / notifications
- Automated duplicate detection beyond the current in-app check
- Rules extraction / parsing
- Any network features (the app is offline-first by design)

Workflow/retrofit scaffolding intentionally **not yet created** (Minimum Mode):
- Full core-8 workflow set
- `prompts/`
- `docs/AI_BUILD_WORKFLOW.md`
- `docs/PROJECT_RULES.md`

## Validation checklist
- [ ] `git status --short` — only intended files changed; no personal/export
      data staged.
- [ ] Browser/manual smoke test of any changed UI areas.
- [ ] Export/import round-trip if export/import was touched.
- [ ] localStorage persistence check (reload page) if storage was touched.
- [ ] Confirm no new network calls, dependencies, or build steps introduced.

## Current next recommended task
Review this Minimum Mode workflow/safety layer (`CLAUDE.md`,
`docs/CURRENT_STATUS.md`, `.gitignore`) while it is unstaged, then decide
whether to commit. No app changes are pending.

## Warnings
- ⚠️ **Personal / exported data must never be committed.** The remote is
  **public**. Exports (JSON/CSV) and backups are private — keep them out of git
  (see `.gitignore`) and verify `git status --short` before any staging.
- ⚠️ **Do not touch `sweepstakes-tracker_local_throwaway`** — the sibling
  throwaway twin folder is off-limits until separately reviewed.
