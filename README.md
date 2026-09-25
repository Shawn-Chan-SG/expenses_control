# College Ledger

A lightweight expense tracker built for two people (shared household/college expenses) to log spending from different devices, see a monthly dashboard, and bulk-import historical data from Excel.

## Files

- `college-ledger.html` — the app. Single-file HTML/CSS/JS, no build step required.

## Two ways to run it

**1. Live, synced version (recommended)**
Open the hosted version here — data syncs automatically between devices/users:
https://claude.ai/artifact/DACyrxSHUquTveV9B7qQr1

Note: this link currently only syncs for people inside the same Claude organization as the owner. If the second user is external, see "Known limitation" below.

**2. Static offline copy**
Open `college-ledger.html` directly in any browser. This works standalone with no login, but does **not** sync between devices — each device/browser keeps its own local data.

## Features

- **Add** — quick entry form for a new expense (date, category, amount, payer, notes)
- **Dashboard** — monthly income vs. budget vs. spend, category breakdown
- **Log** — full transaction history, editable/deletable per entry
- **Settings** — categories, budgets, and payers, seeded from the original `expense control.xlsx` template
- **Import** — bulk-load expenses from an Excel/CSV file in the same shape as `expense control.xlsx`

## Known limitation

The synced version uses Claude's built-in per-artifact database, which is currently restricted to members of the same Claude organization as the owner. If the second user doesn't have a seat in that org, their entries on the live link won't sync — use the static copy on each device instead, or ask about alternative sync options (e.g. a shared Google Sheet or a small hosted backend).

## Source data

Seeded categories, budgets, and payers come from the uploaded `expense control.xlsx` ("College Expense Control" template). Sample transaction rows from that file were intentionally **not** imported — only the real config (categories/budgets) was seeded.

## Publishing to GitHub (optional)

To host this as a static site (e.g. via GitHub Pages):

```bash
git init
git add college-ledger.html README.md
git commit -m "Initial commit: College Ledger expense tracker"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

Then enable GitHub Pages on the repo (Settings → Pages → deploy from `main`) to get a public URL for the static copy. Note the static copy won't have cross-device sync (see "Known limitation").
