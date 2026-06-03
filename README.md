# Sweepstakes Tracker

A **manual-first** sweepstakes research, review, and tracking tool. It's a
**decision-support system, not an auto-entry bot** — it helps you decide which
sweepstakes are worth your time and safe to enter, then tracks what you entered
so you don't create duplicates or break entry limits.

It will **never** create accounts, submit forms, spend money, or bypass
CAPTCHAs, email verification, or rate limits. You always read the official rules
and enter yourself.

## Running it

It's a single file — no install, no server, no account.

- **On your computer:** double-click `sweepstakes.html` to open it in your browser.
- **On your phone (optional):** host it free with GitHub Pages
  (*Settings → Pages → Branch: `main` → Save*), open the link, then "Add to
  Home Screen."

All your data is stored **locally in your browser** on the device you use it on.
Nothing is uploaded anywhere. Use **More → Export** to back up your data, and
**Import** to restore it or move it to another device.

## The workflow

The app walks each opportunity through six steps:

1. **Discovery** — drop links into the **Review** queue as you find them
   (prefer official brand pages over third-party listing sites).
2. **Rules review** — read the official rules and fill in the review form:
   sponsor, prize, value, deadline, eligibility, entry method, frequency,
   whether a purchase is required, and the no-purchase method.
3. **Risk review** — set risk / privacy / time ratings and check off any
   **red flags** (no sponsor, requires payment, "you already won" language, etc.).
4. **Score** — rate seven factors 0–5 (legitimacy, prize value, entry effort,
   eligibility clarity, privacy safety, deadline urgency, repeat-entry value).
5. **Decide** — the app suggests **Pursue / Maybe / Skip / Research more**.
   Strict overrides force a *Skip* or *Research* regardless of the score when
   something is disqualifying (paid entry, no clear sponsor, no official rules,
   you're not eligible, sensitive info demanded before winning, high risk).
6. **Track** — log every entry. The app computes your **next eligible entry
   date** (daily / weekly / monthly / one-time) and warns you before you enter
   too early, exceed the max entries, re-enter a one-time sweepstakes, or enter
   after the deadline.

## The tabs

| Tab | What it does |
|-----|--------------|
| 🏁 **Home** | What to do next: enter today, deadlines within 7 days, items needing review. |
| 📋 **Tracker** | Every opportunity, filterable by status, with deadline countdowns and scores. |
| 🔍 **Review** | A queue for capturing leads fast, then turning them into full reviews. |
| 📝 **Log** | Your full entry history, grouped by date, with rule-concern flags. |
| ⚙️ **More** | Default email, JSON/CSV export, import, reset, and an example loader. |

## Statuses

Researching · Active · Entered · Daily repeat · Weekly repeat · Maybe ·
Skipped · Expired · Not eligible · Won · Disqualified risk

## Try it quickly

Open the app, go to **More → Load Liquid Death example** to see a fully
filled-in opportunity (with an entry already logged) and explore how scoring,
next-eligible dates, and the tracker work.

---

*Manual MVP. Automation (reminders, duplicate detection, rules extraction) is
deliberately deferred until the manual workflow proves useful and safe — and
even then, only low-risk reminders, never auto-entry.*
