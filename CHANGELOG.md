# Changelog

All notable changes to **Paycheck Tracker** are recorded here.
Every entry corresponds to a commit pushed to GitHub.

---

## [2026-05-25]

### `e682060` — First-visit welcome screen
- Added a full-screen welcome overlay that appears only on the first visit
- Large fluid typography (up to 108px) with the headline *"You're earning right now."*
- Brief explanation of the app's purpose and four feature highlight pills
- Smooth fade-in / fade-out animation; dismissed state saved to `localStorage` (`pt_seen`)

### `328ed74` — Biweekly pay frequency + free-form payday date
- Added **Pay Frequency** selector: Monthly or Biweekly (every 2 weeks)
- Monthly: free-form number input for any day 1–31 (replaced the fixed dropdown)
- Biweekly: date picker for a known payday; app calculates every 14-day cycle automatically
- Payday countdown panel updates to show next exact date and per-paycheck amount for biweekly workers
- Changes apply in both the setup screen and the settings modal

### `ca0d69f` — Activate Formspree form submission
- Replaced `YOUR_FORM_ID` placeholder with real Formspree form ID `mdajwwbl`
- Idea submissions from `ideas.html` now land in the Formspree dashboard

### `ed2b70b` — Move Ideas link to topbar
- Relocated the `💡 Ideas` button from the ticker bar to the topbar (next to the ⚙ settings gear)
- Styled in gold so it's visible but not intrusive

### `fcbcbf4` — Ideas page + expanded office humor tickers
- Added `ideas.html`: anonymous idea submission page (no login required)
  - Formspree integration, category chips, emoji picker, featured ideas wall
  - Gold/purple particle effects on successful submission
  - Keyboard shortcut Cmd/Ctrl+Enter to submit
- Expanded `TICKERS` array from 20 → 35 entries with relatable office scenarios:
  - Smelly fish in the microwave, bathroom breaks, irrelevant meetings, daydreaming, chatting with the attractive coworker across from you, and more

### `8031866` — Initial release
- Single-file HTML app (`index.html`) with zero dependencies and no build step
- Real-time earnings counter updating every 100ms (2 decimal places)
- Coin rain particle effect + 3-layer synthesized sound (Web Audio API) on milestone hits
- Growth level system: Rookie Grinder → Financial Freedom (6 levels, XP-based)
- Purchasing power panel, daily progress bar, payday countdown, fun stats
- Office event ticker rotating every ~8 seconds
- Overtime mode (1.5× after work hours)
- Settings modal with all parameters editable post-setup
- `localStorage` persistence — no data leaves the device
- Deployed to GitHub Pages: https://songyangzhou.github.io/work-salary-timer/
- Deployed to Vercel: https://work-salary-timer.vercel.app

---

## How to contribute a change

1. Edit files locally
2. `git add <files>`
3. `git commit -m "type: short description"`
4. `git push origin main`
5. Add an entry to this file in the same commit (or a follow-up commit)

Vercel auto-deploys every push to `main` within ~30 seconds.
