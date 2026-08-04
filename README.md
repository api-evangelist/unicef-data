# UNICEF Data

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
