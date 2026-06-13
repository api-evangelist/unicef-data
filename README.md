# UNICEF Data

UNICEF Data is the official open data platform of the United Nations Children's Fund, providing programmatic access to global child welfare statistics, health and nutrition indicators, education data, child protection metrics, MICS (Multiple Indicator Cluster Survey) results, and SDG indicators for children across countries worldwide.

## APIs

### UNICEF SDMX Data Warehouse API

The primary API is an SDMX REST web service exposing UNICEF's Data Warehouse, which contains 748+ indicators organized into thematic dataflows.

- **Base URL:** `https://sdmx.data.unicef.org/ws/public/sdmxapi/rest/`
- **Documentation:** https://data.unicef.org/sdmx-api-documentation/
- **Explorer:** https://sdmx.data.unicef.org/webservice/data.html
- **Authentication:** None required
- **Formats:** SDMX-JSON, SDMX-XML (v2.0, v2.1), CSV, Excel

**Key dataflows:**
- `MNCH` — Maternal, Child and Newborn Health
- `NUTRITION` — Nutrition indicators
- `PT` — Child Protection
- `HIV_AIDS` — HIV/AIDS indicators
- `EDUCATION` — Education data
- `DM` — Demography
- `GENDER` — Gender-related indicators
- `GLOBAL_DATAFLOW` — Cross-sector global indicators

**Example query:**
```
GET https://sdmx.data.unicef.org/ws/public/sdmxapi/rest/data/UNICEF,GLOBAL_DATAFLOW,1.0/ALB+DZA.MNCH_INSTDEL.?format=sdmx-json
```

**List all dataflows:**
```
GET https://sdmx.data.unicef.org/ws/public/sdmxapi/rest/dataflow/all/all/latest/?format=sdmx-json&detail=full&references=none
```

### UNICEF Reference Data Manager API

Provides structured access to UNICEF reference data including geographic hierarchies and organizational classification codes.

- **Base URL:** `https://rdmapi.unicef.org/api/`
- **Documentation:** https://rdmapi.unicef.org/api/doc/index.html

### UNICEF GeoSight API

Geospatial data platform for visualizing humanitarian and development indicators by geography.

- **Base URL:** `https://geosight.unicef.org/api/v1/`
- **Documentation:** https://geosight.unicef.org/en-us/api/v1/docs/

## Licensing

All UNICEF data is available under the [Creative Commons Attribution 3.0 IGO (CC BY 3.0 IGO)](https://creativecommons.org/licenses/by/3.0/igo/) license. Commercial use is permitted with attribution.

## Pricing

All APIs are free of charge. No API key or registration is required for the SDMX Data Warehouse API.

## Contact

- Email: data@unicef.org
- Website: https://data.unicef.org
- GitHub: https://github.com/unicef
