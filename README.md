# NodeLab

NodeLab is a **standalone**, **single-file**, in-browser tool for pairing **ShotMarker** targets with **chronograph strings** and running node-confidence analysis — **fully locally**.

**No installs. No cloud. No accounts.** Your data stays on your machine.

## Run it
- **Live (GitHub Pages):** https://mrimp.github.io/NodeLab/
- **Offline:** download **`NodeLab_LATEST.html`** from this repo and double-click (Chrome/Edge recommended).

## Quick start
1. Load ShotMarker file(s)
2. Load chrono file(s)
3. **Step 3:** Pair each target to exactly one chrono string
4. Run Analysis
5. Export JSON snapshot (filename includes ShotMarker name + timestamp)

## What it does
- Imports ShotMarker targets and identifies scored shots (sighters excluded from scoring)
- Loads chronograph files and maps them to targets via Step 3 pairing
- Produces ranked results with a confidence badge that **explains without dictating**
- Exports a JSON snapshot:
  `NodeLab_<ShotMarkerName>_<YYYY-MM-DD>_<HHMM>.json`

## Privacy
NodeLab runs entirely in your browser.
**All parsing and analysis runs locally.**

## Screenshots

### Step 3: Pair targets ↔ chrono strings
![Step 3 pairing](docs/screenshots/step3-pairing.png)

### Ranking view
![Ranking view](docs/screenshots/ranking.png)

### Drilldown
![Drilldown](docs/screenshots/drilldown.png)

## Issues / Support
When opening an issue, include:
- what file types you loaded (ShotMarker + chrono)
- the on-screen warning/error text
- a screenshot of Step 3 pairing + results

## Snapshot export format
NodeLab exports analysis results as versioned JSON snapshots for use with companion tools (e.g., BarrelTracker).

The export contract is defined here:
➡️ [docs/SNAPSHOT_SPEC.md](docs/SNAPSHOT_SPEC.md)
