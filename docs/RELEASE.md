# Releases & versioning

NodeLab follows **Semantic Versioning**:

- **MAJOR**: breaking export/schema changes or major UI/workflow changes
- **MINOR**: new features that keep export compatibility
- **PATCH**: bug fixes and small UX polish

## Tag flow (GitHub)

Recommended tag format: `vMAJOR.MINOR.PATCH` (example: `v2.6.4`).

1. Update `NodeLab_LATEST.html`:
   - `APP_VERSION` constant
   - the header pill (top bar) version label
2. Update `CHANGELOG.md`.
3. Commit:
   - `git commit -am "Release vX.Y.Z"`
4. Tag:
   - `git tag -a vX.Y.Z -m "NodeLab vX.Y.Z"`
5. Push:
   - `git push && git push --tags`
6. Create a GitHub Release:
   - attach `NodeLab_LATEST.html`
   - include highlights + known issues

## Release checklist

**Before tagging**
- [ ] Open `NodeLab_LATEST.html` via **file://** (double-click) in Chrome/Edge
- [ ] Open **GitHub Pages** version
- [ ] Run **Offline Self-Test** (expect *0 net calls*)
- [ ] Verify exports/imports:
  - [ ] Export .json
  - [ ] Import .json
  - [ ] Export portable bundle
  - [ ] Import portable bundle
- [ ] Confirm Step workflow:
  - [ ] Step 1: ShotMarker files load
  - [ ] Step 2: Chrono files load
  - [ ] Step 3: Pairing complete warning behaves
  - [ ] Step 4: Analysis runs
  - [ ] Step 5: Results render + drilldown works
- [ ] Check browser console: no uncaught errors
- [ ] Confirm README “Run it” instructions are correct

**After tagging**
- [ ] Create GitHub Release for the tag
- [ ] Attach `NodeLab_LATEST.html`
- [ ] Add release notes summary
