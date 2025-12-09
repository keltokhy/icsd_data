# IDSC Indicator Dataset

This package publishes the cleaned observations extracted from idsc.gov.eg (Egypt's Information and Decision Support Center) using Playwright-based scraping.

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

## Variable Names (Arabic / English)
| Column | Arabic | English |
| --- | --- | --- |
| indicator_id | معرف المؤشر | Indicator ID |
| indicator_nameA | اسم المؤشر (ع) | Indicator name (Arabic) |
| indicator_nameE | Indicator name (E) | Indicator name (English) |
| period | الفترة | Period (YYYY / YYYY-Q# / YYYY-MM) |
| frequency | التكرار الزمني | Frequency (A/Q/M) |
| year | السنة | Year |
| quarter | الربع | Quarter |
| month | الشهر | Month |
| value | القيمة | Value |
| unitA | وحدة القياس (ع) | Unit (Arabic) |
| unitE | Unit (E) | Unit (English) |
| sourceId | معرف المصدر | Source ID |
| periodicityId | معرف التكرار | Periodicity ID |
| periodicityA | التكرار (ع) | Periodicity (Arabic) |
| periodicityE | Periodicity (E) | Periodicity (English) |
| dimensions | الأبعاد | Dimensions |
| dataQuality | جودة البيانات | Data quality |
| changeRate | معدل التغير | Change rate |
