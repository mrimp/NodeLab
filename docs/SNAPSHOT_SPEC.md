# Snapshot Export Spec (NodeLab)

NodeLab exports a single JSON file that contains **raw inputs**, **pairings**, **preferences**, and **results**.
It is designed to be portable between machines and stable for companion tools.

## File naming

`NodeLab_<BaseName>_<YYYY-MM-DD>_<HHMM>.json`

- `BaseName` is derived from the session name (if provided) or the first ShotMarker target/session name.
- Characters are sanitized for Windows/macOS/Linux.

## Top-level shape

```json
{
  "app": {"name": "NodeLab", "version": "2.6.4", "full": "NodeLab v2.6.4"},
  "schema": 1,
  "version": "NodeLab v2.6.4",
  "exportedAt": "2026-01-18T20:15:00.000Z",
  "prefs": {
    "units": "moa",
    "realityMode": false,
    "realityWeights": {"lowN": 0.18, "flags": 0.30},
    "view": {"onlyActionable": false, "onlyPinned": false, "lowConfidence": false, "showPairChecks": false, "openRows": []}
  },
  "units": "moa",
  "sessionName": "",
  "shotmarkerFiles": [{"id": "sm_...", "name": "...csv", "targets": ["...raw text per target..."], "info": null}],
  "chronoFiles": [{"id": "ch_...", "name": "...csv", "shots": [{"v": 2920.3, "time": "01:23.456"}]}],
  "targets": [/* parsed targets */],
  "pairings": {"targetId": "chronoId"},
  "results": {/* computed analysis results */},
  "resultsStale": false
}
```

## Compatibility

- **schema** increments only for breaking changes.
- New optional fields may be added without bumping schema.
- Companion tools should ignore unknown fields.

## Notes

- **Sighters** are preserved in drilldown but excluded from dispersion/confidence/ranking.
- Velocity is treated as **context**, not the primary ranking criterion.
