# Changelog

All notable changes to **NodeLab** are documented here.

NodeLab is a **single-file, fully standalone** browser tool: ShotMarker-first analysis for 1000-yard reality.
Ranking is **vertical-first** (scored shots only); velocity is **context**.

---

## [v2.6.4] — 2026-01-10

### Improved
- Packaging / offline reliability: removed a stray captured stylesheet reference that could break fully-standalone usage.

### Repo
- Added a GitHub Pages root landing (`index.html`) that forwards to `NodeLab_LATEST.html`.
- Synced a versioned release build: `releases/NodeLab_v2_6_4_RELEASE.html`.

---

## [v2.4.3] — 2025-12-23

### Added
- **Garmin Sessions `.xls` multi-sheet support**: each worksheet/tab is imported as its own chrono string (creates multiple chrono slots from one file).
- Chrono loading UI now counts **strings** (not just files) when Garmin session workbooks are used.

### Fixed
- ShotMarker CSV parsing edge cases:
  - Leading empty column + extra trailing field (e.g. `sim_t(...)`) no longer breaks column alignment.
  - Mixed time formats (e.g. `9:00.55 am`) no longer prevent shot rows from being recognized.
- Ensured multi-target ShotMarker archive exports correctly expand into **N targets (strings)**.

---

## [v2.4.1] — 2025-12-22

### Added
- **Compare Grid (aligned, side-by-side)** for up to 3 targets (true metric alignment).
- Compare grid includes **Radial ES (approx)** and respects unit toggle (MOA/mm @ 1000y).
- **Share Report export** (lightweight HTML) includes pinned contenders, compare section, and notes (when present).
- **Collapse all drilldowns** control.
- **Shooter notes** per target + row note icon indicator.

### Improved
- Drilldown uses right-side space properly and spans full table width.

### Fixed
- Multiple UI/runtime issues discovered during live testing (duplicate bindings, undefined helpers, share rendering variables).
- Notes persist reliably through Export/Import.

---

## [v2.3.x] — 2025-12-22

### Added
- **Compare selection** (up to 3) with a raised compare strip.
- **Pin contenders** so top candidates stay visible during iteration.
- **Share Report** button (export lightweight HTML).
- UI layout widened (more room across the app).

### Improved
- Compare strip made sticky (then refined to avoid overlap issues).
- Drilldown layout moved toward a **right-heavy split**.

### Fixed
- Multiple sticky/overlap bugs that hid row checkboxes or blocked unchecking.

---

## [v2.2.x] — 2025-12-22

### Added
- **Shooter Notes** (per target) in drilldown.
- Notes included in **Export .json** and restored on **Import .json**.
- **Tiny note icon** in ranking rows when notes exist.

### Improved
- Confidence transparency: “confidence inputs” surfaced in drilldown (n-shots, penalties, etc.).
- Diagnostics ordering clarified (vertical → horizontal → structure → velocity → sample).

### Fixed
- Early release parsing/build issues (HTML/JS injection causing `Unexpected token '<'`).
- Notes initially displayed but did not persist; fixed by wiring notes to state + export/import.

---

## [v2.1] — 2025-12-22

### Added
- Stable **standalone** NodeLab workflow:
  1) Load ShotMarker target files
  2) Load chronograph files (CSV/XLS/XLSX)
  3) Pair targets ↔ chrono
  4) Run analysis + ranking + drilldown
- **Sighter exclusion rule**: shots tagged `sighter` are visible but excluded from ranking/dispersion/confidence.
- Unit toggle: **MOA @ 1000y** ↔ **mm @ 1000y**.
- Export/Import session as `.json`.

### Improved
- UI polishing: tighter pairing rows, clean dark theme, clear session KPIs.

---

## Notes
- NodeLab’s ranking philosophy is consistent across releases:
  - **Vertical is king** at 1000y
  - **Velocity is context**, not the driver of rank
  - Tool explains; shooter decides

