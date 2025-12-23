# NodeLab

**ShotMarker-first session analysis for 1000-yard reality.**  
NodeLab ranks targets by **vertical dispersion** (scored shots only), surfaces confidence, and flags patterns that matter at 1000 — without telling you what to do.  
**Velocity is context. Vertical is king.**

- ✅ **Standalone**: runs fully locally in your browser (single HTML file)
- ✅ **Match-ready workflow**: ShotMarker archive exports (multi-target) + Garmin Sessions `.xls` (multi-string)
- ✅ **Sighters excluded** from scoring/ranking (still visible for awareness)

## Quick start

### Option A — Run locally (recommended)
1. Download: **`NodeLab_LATEST.html`**
2. Double-click to open in Chrome/Edge (or drag into the browser)
3. Load files and run analysis:
   - Step 1: ShotMarker target exports (`.csv`)
   - Step 2: Chronograph files (`.csv`, `.tsv`, `.xls`, `.xlsx`)
     - Garmin Sessions `.xls` is supported (multi-sheet → multiple chrono strings)
   - Step 3: Pair **1 target ↔ 1 chrono string**
   - Step 4: Run analysis

### Option B — GitHub Pages (shareable URL)
If you enable GitHub Pages for this repo, you can run NodeLab via a URL:
- Settings → Pages → Deploy from branch → `main` / `/ (root)`
- Then open: `https://<your-user>.github.io/<repo>/NodeLab_LATEST.html`

## What NodeLab considers a “target”
ShotMarker archive exports may contain **multiple targets (strings)** inside one CSV.  
NodeLab treats **each string** as one target (so 1 file can become 10+ targets).

## Export / import
NodeLab can export a session `.json` and re-import it later, including:
- pairing state
- pinned/compare state
- **shooter notes** (per target)

## Releases
Versioned builds are in `/releases`.  
`NodeLab_LATEST.html` always matches the most recent release.

## License
MIT — see `LICENSE`.

---

**NodeLab** is shooter-facing: it explains, never dictates.
