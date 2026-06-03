# CLAUDE.md — Sweepstakes Tracker

## Project identity
A **manual-first** sweepstakes research, review, and tracking tool — a
**decision-support system, not an auto-entry bot**. It helps a human decide
which sweepstakes are worth their time and safe to enter, then tracks entries
to avoid duplicates and entry-limit violations. The human always reads the
official rules and enters themselves.

## Single-file app rule
The entire application is **one file: `sweepstakes.html`** (inline HTML, CSS,
and JS). There is no build system, no server, no package manager, no test
framework, and no dependencies. Keep it that way:
- All app logic stays inside `sweepstakes.html`.
- Do not introduce a bundler, framework, server, or external runtime deps.
- Data lives in the browser's `localStorage`; backups are JSON/CSV via the
  in-app Export/Import.
- `README.md` is the canonical user-facing description — do not modify it as
  part of routine workflow changes.

## Hard forbidden items
This app must remain manual and safe. Never add, enable, or assist with:
- **No auto-entry** — no automated submission of sweepstakes entries.
- **No account creation** — no automated signup or registration.
- **No form submission** — no programmatic posting of any external form.
- **No CAPTCHA bypass** — and no defeating email verification or rate limits.
- **No spending/payment automation** — no purchases, no payment flows.
- **No network egress** unless explicitly approved by the user first. The app
  is offline-first and makes no network calls; keep it that way.
- **No committing exported personal data** — exports (JSON/CSV) are private and
  must never be staged or committed. The GitHub remote is **public**.
- **No touching the throwaway twin folder** — the sibling
  `sweepstakes-tracker_local_throwaway` is off-limits until separately reviewed.

## Validation guidance
After any change, validate before considering it done:
- `git status --short` — confirm only intended files changed, and that no
  personal/export data is staged.
- **Browser/manual smoke test** — open `sweepstakes.html` in a browser and
  exercise the UI areas you changed (Home, Tracker, Review, Log, More).
- **Export/import round-trip** — if you touched export or import, export data,
  reset/reload, re-import, and confirm it restores intact.
- **localStorage persistence check** — if you touched storage, make a change,
  reload the page, and confirm the data persisted correctly.

## Commit / push rules
- **No commit without explicit instruction** from the user.
- **No push without explicit instruction** from the user.
- The remote is **public**: privacy-sensitive files (personal exports, backups,
  local data dumps) must **never** be staged. Verify with `git status --short`
  before any staging or commit.
