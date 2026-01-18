# Known limitations / browser notes

This project is intentionally **single-file** and **offline-first**. That comes with a few browser quirks.

## file:// (double-click) quirks

- **Chrome / Edge** (recommended): full functionality, including drag & drop.
- **Firefox**: drag & drop can be more restrictive depending on OS / settings.
- Some security tools / extensions can inject markup into saved HTML files. If you see unexpected overlays or console errors referencing `chrome-extension://...`, try:
  - opening in an **Incognito/Guest** profile,
  - disabling screenshot/overlay extensions,
  - re-downloading `NodeLab_LATEST.html` from the repo.

## Drag & drop permissions

- If drag & drop doesn’t work, use the **Load** buttons instead.
- Some environments (locked-down corporate builds, hardened Windows policies) block dropping files onto local pages.

## Local storage

NodeLab uses **localStorage** for small UI prefs and an **autosave restore** prompt.

- If storage is disabled (private mode, hardened policies), the app will still run, but:
  - autosave/restore is unavailable,
  - some UI prefs won’t persist.

## .xlsx parsing

This build intentionally avoids external dependencies. `.xlsx` support is limited.

- If your chrono export fails, export **CSV** instead.

## GitHub Pages vs file://

Both are supported.

- GitHub Pages runs under `https://...` and generally has fewer file permission quirks.
- file:// runs with stricter drag/drop + storage restrictions on some systems.

Use **Offline Self-Test** (in the app) to confirm:
- no network calls,
- storage availability,
- no external URLs referenced.
