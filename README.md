# IDSC Indicator Dataset

This package publishes the cleaned observations extracted from idsc.gov.eg using Playwright-based scraping and consolidation scripts in this repo.

## Contents
- `idsc_observations.csv` — flattened observations with normalized periods and frequencies.
- `idsc_observations.json` — same data as JSON.

## Schema (idsc_observations)
- `indicator_id`: int
- `indicator_nameA` / `indicator_nameE`: str
- `period`: str — annual `YYYY`, quarterly `YYYY-Q#`, monthly `YYYY-MM`.
- `frequency`: str — `A` (annual), `Q` (quarterly), `M` (monthly).
- `year`, `quarter`, `month`: ints (blank where not applicable).
- `value`: float
- `unitA`, `unitE`: str
- `sourceId`: int
- `periodicityId`: int
- `periodicityA`, `periodicityE`: str
- `dimensions`: str (free text, e.g., “الدولة : مصر”)
- `dataQuality`: str
- `changeRate`: float

## Notes
- Current crawl covers the 48 indicators exposed by the listing endpoint. Only the source/periodicity shown there is included.