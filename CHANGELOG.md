# Changelog

All notable changes to **NodeLab** will be documented in this file.

NodeLab is a **single-file, fully standalone** browser tool: ShotMarker-first analysis for 1000-yard reality.
Ranking is **vertical-first** (scored shots only); velocity is **context**.

---

## [v2.4.1] — 2025-12-22

### Added
- **Compare Grid (aligned, side-by-side)** for up to 3 targets (true metric alignment).
- Compare grid now includes **Radial ES (approx)** and respects the unit toggle (MOA/mm @ 1000y).
- **Share Report export** (lightweight HTML) upgraded:
  - includes pinned contenders
  - includes compare section (when selected)
  - includes notes (when present)
- **Collapse all drilldowns** control for faster scanning.
- **Row-level “Shooter Notes” indicator** (tiny note icon) when notes exist.

### Improved
- Drilldown row now spans full table width (fixed `colspan` mismatch) and **uses right-side space properly**.
- Compare UX hardened:
  - compare controls don’t accidentally open drilldown
  - remove-from-compare actions available directly in compare UI
  - no sticky overlap / “covered checkbox” behavior
- Consistent number formatting and cleaner compare presentation.

### Fixed
- Notes now reliably **persist through Export/Import**.
- Eliminated multiple JS runtime issues discovered during live testing (duplicate bindings, undefined helper references, undefined variables in share rendering).

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

