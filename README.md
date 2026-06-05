# desynpuf-atlas

Population & environmental atlas at H3 res-4 and Census 2020 ZIP5, built
from CMS DE-SynPUF synthetic Medicare claims (~395k synthetic beneficiaries)
joined to public reference data (ACS, EPA PM₂.₅ / ozone LUR, NLCD, CDC SVI,
LandScan, WorldPop, EPA Walkability Index).

**Browse the atlas → https://axleinfo.github.io/desynpuf-atlas/**

## What's here

- `index.html` — the atlas, with a per-source thumbnail grid.
- `manifest.csv` — one row per rendered map; useful for programmatic access.
- `maps/<grain>/<source>/<column>_<year>.png` — the underlying figures.

## How it was generated
desynpuf-link viz bulk 
--tf-nf-root <tf-nf checkout> 
--out-dir build/maps 
--assignment-csv-h3 build/synthetic_h3.csv 
--assignment-csv-zip5 build/synthetic_zips.csv

See [`axleinfo/desynpuf-zip`](https://github.com/axleinfo/desynpuf-zip) for
the pipeline source, methodology, and licensing.

## License

Atlas figures: CC-BY-4.0. Underlying data: see source-specific licenses in
[`axleinfo/terrafusion`](https://github.com/axleinfo/terrafusion).
