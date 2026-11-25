# 🏏 Digvijay Premier League (DPL) — Turf Cricket Tournament Manager

A real-time, mobile-first web and Android/iOS progressive application built to manage every aspect of the **Digvijay Premier League (DPL)** turf cricket tournament—from player registrations and ₹500 entry fee tracking to post-auction team drafting, match scheduling, Cricbuzz-style live ball-by-ball scoring, and tournament MVP leaderboards.

---

## ✨ Key Features

### 1. Player Registration, ₹500 Fee Tracker & Custom Jersey Sizes
* **Live Financial Dashboard:** Real-time KPI summary cards tracking **Total Registered Players**, **Paid (₹500)** count, **Pending Fees**, and **Total Pool Collected (₹)**.
* **One-Tap Fee Management:** Instantly toggle player entry fee statuses between *Pending* and *Paid ₹500*.
* **Custom T-Shirt Size Management:** Select standard sizes (`XS`–`4XL`) or type custom jersey sizes inline, backed by a live **Jersey T-Shirt Size Tally** bar for quick kit ordering.
* **Smart Filtering:** Search players by name or phone number and filter by fee status, playing role (*Batsman, Bowler, All-Rounder, Wicket-Keeper*), or jersey size.

### 2. Custom Team Builder & Post-Auction Draft
* **Full Color Wheel Branding:** Create franchises with custom hex colors via a full HTML5 color wheel with automatic luminance-aware text contrast.
* **Offline Auction Assignment:** Manage an **Unassigned Auction Pool** and assign or release players to franchises right after your offline auction, including appointing team captains `(C)`.

### 3. Match Scheduler & Auto-Updating Points Table
* **Turf Fixture Support:** Schedule matches with flexible turf over limits (**4, 5, 6, 8, 10, or 12 overs**), venue/court details, and match status tracking (*Upcoming, Live, Completed*).
* **Automated Standings:** Automatically calculates **Matches Played (M), Won (W), Lost (L), Tied (T), Points (PTS), and Net Run Rate (NRR)** as soon as matches conclude.

### 4. Cricbuzz-Style Live Scorer & Scorecard
* **Real-Time Live Scoreboard:** Displays runs/wickets, overs bowled, Current Run Rate (CRR), target chase equation (*Need X runs in Y balls*), Required Run Rate (RRR), and a color-coded **Recent Balls** timeline (`0`, `1`, `4`, `6`, `W`, `WD`, `NB`).
* **Complete Ball-by-Ball Engine:** Supports automatic strike rotation, wide/no-ball extra handling, wicket dismissal modals with fielder attribution, over-end bowler prompts, a full **Undo Last Ball** stack, and detailed **1st & 2nd Innings Scorecards**.

### 5. Live Tournament Stats & Leaderboards
* **Orange Cap:** Tracks top run-scorers with innings, average, strike rate, `4s`, and `6s`.
* **Purple Cap:** Tracks leading wicket-takers with overs, economy rate, and best bowling figures (`BBI`).
* **DPL MVP Points:** Ranks top all-round performers using live impact points (`1 pt/run`, `+2 bonus/4`, `+4 bonus/6`, `25 pts/wicket`, `10 pts/catch, stumping, or run-out`).

### 6. Real-Time Cloud Sync & Role-Based Access
* **Firebase Realtime Database Sync:** Syncs all rosters, scores, and stats across every player's and spectator's phone in real time (`Cloud Live`), with automatic offline caching fallback.
* **Viewer Mode vs. Admin PIN Lock:** Opens in safe, read-only **Viewer Mode** for players and spectators, while organizers unlock full editing and live scoring controls using a customizable **Admin PIN** (default: `2026`).

---

## 🛠️ Tech Stack

* **Frontend:** Single-file HTML5, Vanilla JavaScript (ES6+), Tailwind CSS, Font Awesome, Google Fonts (`Inter` & `JetBrains Mono`)
* **Backend / Cloud Sync:** Firebase Realtime Database (REST + real-time polling/sync with `localStorage` offline fallback)
* **Mobile / App Packaging:** Progressive Web App (PWA) ready for Android/iOS *Add to Home Screen* and TWA/WebView `.apk` / `.aab` packaging

---

## 🚀 Quick Setup & Deployment

1. **Clone or Download:** Download `index.html` from this repository.
2. **Configure Firebase (Optional if using your own DB):** Open `index.html` and set your Firebase Realtime Database URL in the configuration block.
3. **Host Live:** Enable **GitHub Pages** (`Settings → Pages → Branch: main / root`) or deploy to Netlify/Vercel for an instant HTTPS link.
4. **Install as Mobile App:**
   * **Android:** Open the live link in Chrome → tap **⋮** → **Add to Home screen** (or package via PWABuilder / WebIntoApp for `.apk` / Play Store `.aab`).
   * **iPhone:** Open the live link in Safari → tap **Share** → **Add to Home Screen**.

---

## 🔐 Default Admin Access

* **Viewer Mode:** Enabled by default on page load (read-only live scores, rosters, and stats).
* **Admin Mode PIN:** `2026` *(can be changed anytime inside the header PIN settings once unlocked)*.
