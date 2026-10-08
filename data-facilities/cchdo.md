---
title: "CLIVAR and Carbon Hydrographic Data Office"
short_name: "CCHDO"
homepage: "https://cchdo.ucsd.edu/"
guidance_status: "draft"
last_reviewed: "2026-10-08"
maintained_by: []
reviewed_by: []
tags:
  - "hydrography"
  - "CTD"
  - "bottle data"
  - "GO-SHIP"
access_methods:
  - "website"
  - "file-download"
  - "bulk-download"
  - "data-service"
---

# CLIVAR and Carbon Hydrographic Data Office (CCHDO)

> **About this page:** This preliminary, exploratory draft helps people and AI agents discover CCHDO data and interpret them responsibly. It does not replace CCHDO documentation. Sources were checked on 2026-10-08. Core sections, access modules, interpretation guidance, and two tested retrieval examples are drafted. Reviewer, maintenance arrangements, and review cadence are TBD; specific service details are deferred below.

## Core: At a glance

**What it is:** CCHDO provides global ship-based CTD and bottle hydrographic data from GO-SHIP, WOCE, CLIVAR, and other repeat hydrography programs. [CCHDO homepage](https://cchdo.ucsd.edu/)

**Authoritative role:** CCHDO is the repository for global GO-SHIP CTD and bottle data and a Data Assembly Center for physical and chemical hydrographic profiles. [Data scope](https://learning.cchdo.io/policies_and_procedures/data_scope), [submission guide](https://learning.cchdo.io/submitting_data/detailed_guide)

CCHDO assembles and distributes standardized hydrographic datasets, checking format, parameter names, units, and flags. CCHDO also supports scientific quality control; ultimate decisions on scientific quality control remain with the data originators whenever possible. This description of responsibilities was confirmed by Carolina Berys, CCHDO Lead Data Manager, during profile development on 2026-10-08.

**Use this facility when:**

- Finding hydrographic cruises, repeat-section occupations, CTD profiles, or bottle observations.
- Obtaining data together with the identifiers, documentation, units, quality flags, and citation information needed for analysis.

**Do not assume:**

- Every measurement collected on a GO-SHIP cruise is held here: the submission guide excludes underway and ADCP data from CCHDO management. [Submission guide](https://learning.cchdo.io/submitting_data/detailed_guide)
- A search result establishes that the requested parameter, coverage, or processing status is available; check the selected data and documentation.

**Primary entry point:** [CCHDO](https://cchdo.ucsd.edu/).

## Core: What the facility contains

Holdings include CTD profiles, bottle hydrographic observations, and associated cruise documentation. CCHDO's accession priorities emphasize GO-SHIP and associated cruises, largely full-depth surveys across substantial ocean sections; other qualifying hydrographic data are accepted as resources allow. These priorities do not establish complete geographic or temporal coverage. [Data scope](https://learning.cchdo.io/policies_and_procedures/data_scope)

Available format families include WHP-Exchange, CF/netCDF, legacy WHP netCDF, and WOCE. Individual cruises need to be checked for actual file availability. [File formats](https://learning.cchdo.io/getting_started/file_formats)

**Scope of this profile:** Discovery and interpretation of CCHDO's public CTD and bottle holdings. CCHDO also manages public and non-public CTD data for Argo and OceanSITES; this work is noted here for context. [CCHDO homepage](https://cchdo.ucsd.edu/)

## Core: How to start a search

Establish the place, time period, cruise or vessel if known, required observations, CTD versus bottle data, and desired output. An EXPOCODE is useful but is not required to begin discovery.

The [advanced cruise search](https://cchdo.ucsd.edu/search/advanced) accepts text, geography, and dates. Text can match EXPOCODE, ship, section, program, and other cruise metadata; multiple terms and constraints narrow the result together. Bounding-box searches require a station within the box and exclude cruises without trackline metadata. Date filters operate on cruise start dates, not on every observation date.

For observations within particular spatial, temporal, pressure, or parameter ranges, the [Simple Profile Search](https://cchdo.github.io/erddap_search/) provides a profile-oriented route to the linked CTD and bottle ERDDAP datasets. See the [data-services module](#access-module-data-services) for current limitations and outstanding service questions.

## Core: Important entities and identifiers

| Entity | Identifier | Meaning and scope | Common pitfalls |
|---|---|---|---|
| Cruise | `EXPOCODE` | Expedition identifier | Use the recorded value; do not reconstruct it from vessel and date. |
| Repeat section | `SECT_ID` | WOCE/GO-SHIP section designation | A section can have multiple occupations; it does not identify one cruise. |
| Station | `STNNBR` | Originator's station identifier | Preserve text identifiers; retain cruise context. |
| Cast | `CASTNO` | Originator's cast number | Retain cruise and station context. |
| Sample | `SAMPNO` | Sample identifier | Values may be nonnumeric; retain cruise, station, and cast context. |
| Sampling bottle | `BTLNBR` | Identifier attached to the sampling device | Do not assume it is interchangeable with the sample identifier. |

These fields are defined in the [Exchange parameter reference](https://exchange-format.readthedocs.io/en/latest/parameters.html). A combined file or CTD archive may contain more than one EXPOCODE.

The current [bottle specification](https://exchange-format.readthedocs.io/en/latest/bottle.html) uses the combination of EXPOCODE, station, cast, and sample to distinguish rows representing bottle-closure events. For older files, preserve the identifiers as supplied and consult the applicable specification and cruise documentation before joining records. Report ambiguous or conflicting identifiers rather than silently coercing them into a modern convention.

## Core: Recommended discovery and access path

**Recommended routing:** Carolina Berys confirmed cruise downloads, bulk downloads from search results, ERDDAP profile subsets, and archival snapshots as appropriate access routes on 2026-10-08.

1. Start at [CCHDO](https://cchdo.ucsd.edu/) for individual cruises or bulk downloads from cruise search results. Use [Simple Profile Search](https://cchdo.github.io/erddap_search/) for subsets of individual profiles, after checking variable availability. Use archival snapshots for a preserved version of the public collection. See the [file and bulk download module](#access-module-file-and-bulk-download).
2. Confirm identifiers, vessel, dates, location, and required observations against the selected result and files.
3. Retrieve the data and available cruise documentation. Distinguish assembled **Dataset** files from **Unmerged Data as Received**, as described below. Choose a format based on the user's software and task using the [format guide](https://learning.cchdo.io/getting_started/file_formats).
4. Inspect units, quality flags, provenance, and upload/update and submission dates before analysis. Record the source URL, identifiers, filename, retrieval date, and supplied version information; do not assign an undocumented preliminary, current, or superseded label.
5. Follow [CCHDO's citation guidance](https://learning.cchdo.io/policies_and_procedures/how_to_cite) for the archival snapshot and individual cruises used.

If discovery fails, broaden potentially excluding filters and verify the identifiers. If access fails or the intended product remains ambiguous, report the problem and seek clarification from the user or CCHDO. Do not silently substitute another cruise, occupation, or product.

# Interchangeable access modules

## Access module: Website search and browsing

**Status:** Supported public access route; confirmed by Carolina Berys on 2026-10-08.

**Entry points:** [CCHDO homepage](https://cchdo.ucsd.edu/), [advanced cruise search](https://cchdo.ucsd.edu/search/advanced).

Search with an EXPOCODE, vessel, section, program, or other known cruise information; open the matching cruise record to select data and documentation, or use **Bulk Download Options** on the results page. Use the spatial and date constraints described in [How to start a search](#core-how-to-start-a-search). Confirm the intended occupations before choosing files.

For an empty or ambiguous result, check spelling and identifiers, then relax constraints individually. Do not interpret a failed constrained search as proof that CCHDO lacks the observations.

## Access module: File and bulk download

**Status:** Supported public access routes: individual cruise files, bulk downloads from search results, and archival snapshots. Confirmed by Carolina Berys on 2026-10-08.

**Documentation:** [File formats](https://learning.cchdo.io/getting_started/file_formats), [CCHDO data tutorial](https://learning.cchdo.io/getting_started/quick_start_guides/notebooks/explore_cchdo).

For a cruise, use the files linked from its cruise page and retain the available documentation. **Dataset** contains assembled files checked for format consistency. **Unmerged Data as Received** contains recent submissions that have not yet been checked for consistency and incorporated into that Dataset; they are supplied as received. If unsure which files to use, start with Dataset files and seek clarification about relevant unmerged submissions. These section meanings were checked on the public website and confirmed in discussion with Carolina Berys on 2026-10-08.

For a group of cruises:

1. Submit a search defining the intended set of cruises and check the matches.
2. Open **Bulk Download Options** on the results page. Choose the required format and data type: Exchange, WHP netCDF, or CF/netCDF for bottle or CTD; WOCE for bottle, CTD, or summary; or PDF/text documentation.
3. Refine the actual search to change the download scope. The separate **Filter Table** control changes the displayed table and map; it does not change the bulk-download links.
4. Retain the search URL, chosen format/type, downloaded package, and retrieval date; inspect the delivered files against the intended cruise set.

These controls were checked in the public HTML and JavaScript of the [P16 search-results page](https://cchdo.ucsd.edu/search?q=P16) on 2026-10-08; the distinction between search and table-filter scope is based on that code inspection, not a runtime download test. An archive was not generated. Archive format, practical size limits, and treatment of cruises lacking the selected file type are unverified and deferred for a later update by Carolina Berys.

**Choosing a format:** Ask what software and analysis the user intends to use, then select a compatible format actually offered for the data. This approach was confirmed by Carolina Berys on 2026-10-08. The `.nc` extension alone does not establish which netCDF conventions apply.

| Format | When to choose it and what to check |
|---|---|
| WHP-Exchange | For workflows that read hydrographic text files or require direct inspection of headers and tabular values. Ensure the reader handles Exchange headers, units, missing values, and flags. |
| CF/netCDF | For software that uses CF metadata and profile arrays, including the xarray workflow demonstrated in CCHDO's tutorial. Check variable attributes and array dimensions. |
| Legacy WHP netCDF | When existing software expects this COARDS-compliant convention. Verify compatibility separately from CF/netCDF. |
| WOCE | When a workflow specifically requires the legacy WOCE formats. Consult the corresponding format documentation. |

For the public collection in bulk, follow **Download Everything** on the [homepage](https://cchdo.ucsd.edu/) to the [archival collection](https://doi.org/10.6075/J0CCHAM8), then choose and record a snapshot version. CCHDO describes snapshots as monthly; verify the dates actually available rather than assuming a snapshot equals today's holdings.

Record the selected file or archive, source, format, and retrieval date. If a download or archive is inaccessible, report that limitation and seek assistance; do not invent a replacement link or snapshot version. Snapshot contents, package sizes, and checksums have not yet been inspected in this draft.

## Access module: Data services

**Status:** Supported public route for profile subsets, confirmed by Carolina Berys on 2026-10-08; served through NOAA PMEL ERDDAP. Update timing relative to cruise files and operational service expectations remain unverified.

**Service type:** ERDDAP tabledap.

**Entry points:** [Simple Profile Search](https://cchdo.github.io/erddap_search/), [CTD dataset `cchdo_ctd`](https://data.pmel.noaa.gov/generic/erddap/tabledap/cchdo_ctd.html), [bottle dataset `cchdo_bottle`](https://data.pmel.noaa.gov/generic/erddap/tabledap/cchdo_bottle.html).

The simple interface offers CTD/bottle selection and filters for position, pressure, dates, EXPOCODE, section, and parameter values. Parameter-value filters require both minimum and maximum values. It offers a choice of download formats and a query URL that can be saved.

**Variable coverage:** ERDDAP omits some sparse variables, including identifiers and other non-core variables; Carolina Berys clarified that these omissions do not concern core measurements. Check the [variable availability table](https://hydro.readthedocs.io/en/latest/erddap.html), which lists netCDF variable names, units, and ERDDAP inclusion. At this review it is labeled for CCHDO parameters version 2026.5.0. Consult the linked table rather than treating a copied list as permanent.

The ERDDAP forms allow selection of variables and constraints. Inspect the chosen dataset's schema as well: the CTD and bottle variables differ. If a needed variable or identifier is not available through ERDDAP, retrieve the relevant cruise files, individually or through search-results bulk download. Its absence from ERDDAP does not establish absence from CCHDO holdings.

**Usage guidance:** Preserve the dataset ID, query URL, selected variables, constraints, and retrieval date. A query that can be rerun does not identify an immutable version. If a request fails or returns no observations, verify the schema and constraints, then cross-check cruise discovery. Report unresolved discrepancies. Request-size limits and rate expectations remain unverified. The bounded CTD request in the examples below was tested; this does not establish coverage or behavior for other requests.

# Interpretation and trust

## Recommended: Data and metadata interpretation

- Identify the specific format before reading it: CF/netCDF and legacy WHP netCDF have different conventions. [Format guide](https://learning.cchdo.io/getting_started/file_formats)
- For WHP-Exchange, preserve header comments, read the parameter and unit lines together, and recognize missing-value markers. Older files can use decimal variants of the documented `-999` marker; follow the specification and parameter context. [Common format features](https://exchange-format.readthedocs.io/en/latest/common.html)
- Interpret quality flags using the definitions appropriate to CTD measurements, discrete water-sample measurements, or the sampling bottle itself. These are distinct flag sets; consult the tables linked from [Data quality evaluation and data quality flags](https://learning.cchdo.io/submitting_data/detailed_guide#data-quality-evaluation-and-data-quality-flags).
- **Fitness for use is the user's decision.** CCHDO supplies quality-flag definitions and does not prescribe a default analysis filter. This was confirmed by Carolina Berys on 2026-10-08. Help the user determine which observations suit the intended analysis; preserve the supplied data and flags, and document any inclusion/exclusion criteria and conversions. Do not silently filter observations or present an agent-selected filter as a CCHDO recommendation.

## Core: Provenance, versions, and citation

Cruise reports are the primary cruise documentation when available; accompanying materials can include investigator and data-quality examination reports. Read these alongside the data. [Cruise documentation](https://learning.cchdo.io/policies_and_procedures/cruise_documentation)

Exchange creation stamps and comments can supply file-creation and change information. Do not treat a file-creation date as the date the observations were collected. [Common format features](https://exchange-format.readthedocs.io/en/latest/common.html)

CCHDO recommends citing the UC San Diego Library archival snapshot version closest to the data-access date, using that version's supplied citation and DOI. Describe the subset used. Where individual-cruise citation is reasonable, retain the requested provider citation from the file header. The official guidance also explains using header or “Dataset isBasedOn” information. [How to cite CCHDO data](https://learning.cchdo.io/policies_and_procedures/how_to_cite)

**Dates and file status:** Cruise pages do not explicitly classify files as preliminary, current, or superseded. Compare upload/update and submission dates to identify newer files, and consult the associated Data History notes to understand their relationship. Check **Unmerged Data as Received** for submissions not yet incorporated into the assembled Dataset. A later date establishes a later event; it does not by itself establish scientific finality or replacement of the entire assembled dataset. The date-based guidance and section name were confirmed by Carolina Berys on 2026-10-08.

**Reproducibility guidance:** Retain the downloaded files, source URLs, formats, and access dates alongside the snapshot citation. A citation to the nearest-date snapshot does not by itself verify that it contains an exact copy of a file obtained from the live website. Check snapshot contents before claiming an exact match.

Check cruise-level license and attribution information: the aggregate collection is CC0, while individual cruises may carry CC BY terms. [Data license and DOIs](https://learning.cchdo.io/policies_and_procedures/data_license)

## Core: Known limitations and failure modes

| Situation | Response |
|---|---|
| Spatial or temporal cruise search misses expected data | Recheck station/trackline availability and cruise-start-date filtering; broaden the search. [Search behavior](https://cchdo.ucsd.edu/search/advanced) |
| A user expects Filter Table to limit a bulk download | Refine the submitted search instead; check the search URL and download scope. [Search-results controls](https://cchdo.ucsd.edu/search?q=P16) |
| A section match is mistaken for a particular occupation | Verify EXPOCODE, dates, and vessel before selecting files. |
| Files contain multiple cruises or inconsistent identifiers | Inspect identifiers in the records; resolve conflicts before combining observations. [Identifier reference](https://exchange-format.readthedocs.io/en/latest/parameters.html) |
| A required variable or identifier is absent from ERDDAP | Check the [availability table](https://hydro.readthedocs.io/en/latest/erddap.html) and selected dataset schema, then inspect cruise files through individual or bulk download. |
| A newer submission is mistaken for a complete replacement or a final product | Compare the relevant dates, section, and history notes; distinguish unmerged submissions from assembled Dataset files and report unresolved relationships. |
| An analysis applies an unexplained quality-flag filter | Consult the appropriate flag definitions, have the user determine fitness for use, and document the selected criteria. CCHDO does not prescribe a default analysis filter. |
| Requested measurements, documentation, or product status cannot be established | Report the gap and ask for clarification; do not infer completeness or finality. |
| A source or archive cannot be accessed | Report the failed access path, retain the documented citation guidance, and seek assistance without inventing a version or DOI. |

# Examples and verification

## Recommended: Example tasks

These examples were checked on 2026-10-08. The recorded results are observations from that date, not guarantees that live holdings or query results will remain unchanged. Verification covers retrieval and basic structural interpretation; fitness for a scientific analysis remains the user's decision.

### Example: Retrieve bottle data and inspect oxygen flags

**User question:** Obtain the bottle oxygen observations for cruise `33RO20161119` and identify their units and supplied quality flags.

**Required clarification:** Establish software/format needs. Before using the observations in an analysis, establish the intended use and user-selected filtering criteria.

**Approach:** Locate the [cruise Dataset](https://cchdo.ucsd.edu/cruise/33RO20161119), choose a compatible format, and retain identifiers, units, flags, and file provenance. For this check, the [linked Exchange bottle file](https://cchdo.ucsd.edu/data/42947/33RO20161119_hy1.csv) was downloaded and parsed through its `END_DATA` marker.

**Verified evidence:** File stamp `BOTTLE,20250405CCHHYDRO`; 5,099 data rows and 93 columns, all for the requested EXPOCODE. `OXYGEN` units were `UMOL/KG`. The `OXYGEN_FLAG_W` counts were 4,529 for flag 2, 53 for flag 3, 31 for flag 4, 415 for flag 6, and 71 for flag 9. No quality-flag filter was applied. Interpret each flag using the [water-sample definitions](https://learning.cchdo.io/submitting_data/detailed_guide#data-quality-evaluation-and-data-quality-flags).

**Common failure and response:** Treating every row as ready for the same analysis, or applying a hidden flag filter. Preserve the observations and flags, have the user determine fitness for use, and record any subsequent filtering. Follow the snapshot citation guidance above.

### Example: Retrieve a bounded CTD subset with its flags

**User question:** Retrieve CTD temperature at pressures up to 10 dbar for cruise `33RO20161119`, station `1`, cast `3`, including the temperature quality flags.

**Required clarification:** Confirm pressure units, station/cast identity, and desired variables. Obtain the user's filtering criteria before calculating an analytical result.

**Approach:** Use the CTD ERDDAP dataset and retain identifiers, time, position, pressure, temperature, and its quality flag. [Tested CSV request](https://data.pmel.noaa.gov/generic/erddap/tabledap/cchdo_ctd.csv?expocode,station,cast,time,latitude,longitude,pressure,ctd_temperature,ctd_temperature_qc&expocode=%2233RO20161119%22&station=%221%22&cast=3&pressure%3C=10).

**Verified evidence:** Eight rows, with the requested cruise/station/cast and pressures from 3 to 10 dbar. The response reported temperature in `degree_C`; six rows carried temperature flag 2 and two carried flag 3. Both were retained. Interpret these using the CTD definitions in the [quality-flag tables](https://learning.cchdo.io/submitting_data/detailed_guide#data-quality-evaluation-and-data-quality-flags).

**Common failure and response:** Omitting quality flags from the variable selection or silently excluding flagged observations. Return the flags and explain their definitions; preserve the query and retrieval date. A saved query is not an immutable snapshot.

# Page ownership

**Prepared by:** Carolina Berys, CCHDO Lead Data Manager, with AI assistance for source research and drafting.

**Facility review:** Full-profile facility review has not been completed. Reviewer and review cadence: TBD. During draft development on 2026-10-08, Carolina Berys confirmed the public-holdings scope, assembly and scientific quality-control responsibilities, access routing including search-results bulk downloads, ERDDAP's sparse-variable coverage limitation, selection of formats by software and task, snapshot-DOI citation, use of dates and Unmerged Data as Received to understand newer submissions, and user responsibility for fitness-for-use and quality-flag filtering decisions. Guidance status remains Draft.

**Last checked:** 2026-10-08. Public documentation, quality-flag definitions, and the ERDDAP variable-availability table were read. Cruise-page section labels and dates were checked directly. The reviewer-supplied cruise used to explain unmerged submissions is excluded from this profile. Search-results bulk controls and link behavior were inspected in public HTML and JavaScript; no bulk archive was generated. The two retrieval examples above were tested, including basic checks of identifiers, units, and flags. The archival collection DOI resolved to a library access-denied page in the research tool, so individual snapshot contents were not verified. These checks do not confer Cluster-tested status.

**Maintained by:** TBD.

**Next review:** TBD.

**How to report a problem:** For CCHDO data or documentation questions, contact [CCHDO](mailto:cchdo@ucsd.edu). Profile corrections can be proposed through the [project contribution process](../CONTRIBUTING.md).

**Change history:** 2026-10-08 — Initial draft covering discovery, access, and interpretation. Carolina Berys confirmed scope and responsibilities, access routing, ERDDAP variable coverage, format-selection guidance, snapshot citation, interpretation of file dates and unmerged submissions, and user responsibility for fitness-for-use decisions. Two bounded retrieval examples were tested. Bulk package details were deferred for a later update.

## Open decisions for the next passes

1. Identify a profile reviewer and maintainer, and set a review cadence.
2. Complete a full profile review when those arrangements are established.

## Deferred follow-up

- **Carolina Berys — later update:** Establish search-results bulk archive format, practical size limits, and treatment of cruises missing the requested file type. These are currently unknown and must not be inferred.
- **Service details not yet verified:** ERDDAP update timing relative to cruise files and operational request limits. Record these if authoritative information becomes available.
