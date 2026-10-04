# RouteSpend OSM geometry export

Release: `geometry-2026-10-04`  
Dataset version: `2026-10-04-odbl-v1`  
Snapshot/build date: `2026-10-04`  
Schema version: `1`

This package contains only the OpenStreetMap-derived geometry and topology
database used by RouteSpend for toll-route matching. It includes stable geometry
identifiers, OSM object references, coordinates, selected OSM tags, and
OSM-derived matching/topology annotations.

It does **not** contain tariff prices, origin/destination matrices, calendars,
pricing rules, coverage logic, application code, or any RouteSpend business
logic.

## Attribution and licence

Data © OpenStreetMap contributors.

- OpenStreetMap copyright and attribution: https://www.openstreetmap.org/copyright
- Licence: Open Database License 1.0 (ODbL 1.0)
- Full licence text: https://opendatacommons.org/licenses/odbl/1-0/

The database in `routespend-osm-geometry-2026-10-04-odbl-v1.json.gz` is made available under ODbL 1.0. See
`LICENSE` for the package notice.

## Files

- `routespend-osm-geometry-2026-10-04-odbl-v1.json.gz` — canonical JSON payload compressed with deterministic gzip.
- `manifest.json` — version, schema, record count, provenance and archive checksum.
- `SHA256SUMS` — SHA-256 checksums for all release files except itself.
- `README.md` — this document.
- `LICENSE` — ODbL 1.0 licence notice.

Verify the package with:

```sh
sha256sum -c SHA256SUMS
```

The JSON archive has one top-level `records` array. Every record identifies its
OSM provenance and contains geometry only; consumers must not infer tariffs from
this package.
