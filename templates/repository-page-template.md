---
title: "[Repository name]"
short_name: "[Common abbreviation]"
homepage: "https://example.org"
guidance_status: "draft"
last_reviewed: "YYYY-MM-DD"
maintained_by:
  - "[Person, team, or organization]"
reviewed_by:
  - "[Repository representative, if applicable]"
tags:
  - "[discipline, data type, region, or program]"
access_methods:
  - "website"
  # Other examples: file-download, bulk-download, data-service, api, webpage-extraction, agent-skill, mcp
---

# [Repository name]

> **About this page:** This guidance helps people and AI agents decide when and how to use [repository]. It does not replace the repository's authoritative documentation. Links and access instructions were last reviewed on [date].

<!--
TEMPLATE INSTRUCTIONS

- Complete every CORE section.
- Keep only the ACCESS MODULES that apply to this repository.
- Recommended and optional sections may be removed when they add no value.
- Prefer concise explanations and links to authoritative documentation.
- Write a self-contained page: a user may give an agent only this URL.
- Clearly label unsupported, experimental, or unofficial interfaces.
- Delete all drafting comments before publishing.
-->

## Core: At a glance

**What it is:** [One or two sentences describing the repository.]

**Authoritative role:** [State what the repository is authoritative for, including any formal program or archival role. If it is not authoritative, explain its role without implying otherwise.]

**Use this repository when:**

- [Task, question, data type, region, program, or collection]
- [Another appropriate use]

**Do not assume:**

- [Important boundary, common misconception, or content the repository does not hold]
- [Another limitation]

**Primary entry point:** [Human-facing search, catalog, or landing-page URL]

## Core: What the repository contains

Summarize the repository's major holdings. Describe the relevant scientific domains, platforms, programs, geographic and temporal coverage, data types, processing levels, and product types.

Avoid claiming comprehensive coverage unless that claim is documented by the repository.

## Core: How to start a search

Describe the information a user or agent should provide. Include the most useful starting points, for example:

- geographic area or bounding box;
- time period;
- vessel, platform, or instrument;
- cruise name or identifier;
- program or project;
- parameter or observed property;
- station, cast, profile, sample, or deployment; and
- desired file format or processing level.

Explain which inputs work best and which commonly fail. If a formal identifier is not required for discovery, say so.

## Core: Important entities and identifiers

Define the entities and identifiers needed to use this repository correctly.

| Entity | Identifier or name | Meaning and scope | Common pitfalls |
|---|---|---|---|
| [Cruise, dataset, vessel, station, file, etc.] | [Identifier] | [What it identifies and where it is unique] | [Aliases, formatting, ambiguity, or reuse] |

Explain relationships among entities, such as cruise → station → cast → file. Link to authoritative schemas, vocabularies, identifier documentation, or crosswalks.

## Core: Recommended discovery and access path

Give the preferred sequence for a typical user. Keep it short and link to the applicable access modules below.

1. [Where and how to search]
2. [How to confirm that a result is the intended dataset or cruise]
3. [How to retrieve the data and metadata]
4. [How to identify the version, provenance, and citation]

State what an agent should do when the preferred path fails. Do not direct agents to an unsupported interface without labeling it clearly.

---

# Interchangeable access modules

<!-- Keep, reorder, or remove the following modules to match the repository. -->

## Access module: Website search and browsing

**Status:** [Supported / Experimental / Unsupported]

**Entry point:** [URL]

Explain how to navigate or search the public website, including effective fields, filters, result pages, pagination, and how to reach files and metadata. Describe common dead ends or misleading results.

## Access module: File and bulk download

**Status:** [Supported / Experimental / Unsupported]

**Documentation:** [URL]

Describe direct file downloads, manifests, packages, bulk exports, object storage, FTP, or other download mechanisms. Include naming conventions, formats, checksums, compression, expected size, and any limits.

## Access module: Data services

**Status:** [Supported / Experimental / Unsupported]

**Service type:** [ERDDAP / THREDDS / OPeNDAP / STAC / SOS / other]

**Documentation or endpoint:** [URL]

Explain how to discover datasets and make a basic request. Document important service-specific constraints, identifiers, output formats, and examples.

## Access module: Public API

**Status:** [Supported / Experimental / Internal / Unadvertised / Deprecated]

**Documentation:** [URL]

**Base URL:** [URL]

Describe supported operations, authentication, pagination, rate limits, versions, error responses, and service expectations. Provide one minimal request and expected response shape. Clearly distinguish technical availability from a supported public contract.

## Access module: Webpage extraction fallback

**Status:** [Permitted / Discouraged / Prohibited / Policy not documented]

Use only when a preferred machine-readable method is unavailable. State which public pages may be extracted, what fields are present, and whether permission or coordination is required.

Document request-rate expectations, caching, pagination, dynamically rendered content, embedded structured data, fragile selectors, validation checks, and explicit stop conditions. Do not describe methods that bypass authentication, access controls, or repository policy.

## Access module: Agent guidance and skills

**Status:** [Repository-maintained / Community-contributed / Experimental]

List available agent-oriented resources and explain how to use them.

| Resource | Purpose | Location | Owner/version |
|---|---|---|---|
| `AGENTS.md`, `llms.txt`, `SKILL.md`, notebook, prompt, or other guide | [What it helps accomplish] | [URL] | [Owner and version] |

Describe any platform requirements and whether the resource must be cloned, installed, or explicitly supplied to a chat interface.

## Access module: MCP or StaticMCP-style resources

**Status:** [Supported / Experimental / Not offered]

**Type:** [Conventional MCP / StaticMCP-style experiment / other]

**Documentation:** [URL]

List the resources or tools exposed, supported clients, transport, authentication, permissions, service expectations, and known limitations. For a StaticMCP-style resource, state that the approach is emerging, identify the bridge dependency, and document how and when static responses are regenerated.

---

# Interpretation and trust

## Recommended: Data and metadata interpretation

Explain file formats, schemas, units, quality flags, fill values, coordinate conventions, processing levels, product status, and any domain knowledge needed to avoid incorrect use. Link to detailed references.

## Core: Provenance, versions, and citation

Explain how to determine:

- the origin of data and metadata;
- whether a product is current, preliminary, superseded, or preserved;
- version or update dates;
- relationships to original submissions and derived products;
- the preferred citation; and
- relevant persistent identifiers.

## Core: Known limitations and failure modes

Document problems an agent should recognize and report rather than silently work around. Examples include incomplete coverage, broken external links, inconsistent identifiers, incorrect spatial bounds, delayed updates, combined datasets, ambiguous versions, or fields that should not be treated as authoritative.

For each important failure mode, state the safe response: retry differently, verify against another source, ask the user, contact the repository, or stop.

## Recommended: Cross-repository relationships

Describe how this repository relates to other repositories, programs, operators, and archives.

| Related repository | Relationship | Shared or mapped identifiers | Which source to use when |
|---|---|---|---|
| [Repository] | [Archive, originator, aggregator, complementary holdings, etc.] | [Identifiers] | [Decision guidance] |

Document differences or disagreement openly rather than forcing a single answer.

## Recommended: Responsible and acceptable use

Summarize licensing, attribution, authentication, rate limits, automation policies, restricted or sensitive holdings, and privacy or security considerations. Link to authoritative policies.

# Examples and verification

## Recommended: Example tasks

Provide two or three realistic, tested examples.

### Example: [Task name]

**User question:** [Natural-language question]

**Required clarification:** [Information the agent should request rather than assume]

**Recommended approach:** [Short workflow]

**Expected evidence:** [What sources, identifiers, files, or metadata should be returned]

**Common failure:** [Likely error and how to detect it]

## Optional: Machine-checkable tests

Link to test prompts, fixtures, validation scripts, or expected results maintained elsewhere in this project.

# Page ownership

**Prepared by:** [Name or organization]

**Repository review:** [Reviewer and date, or “Not yet repository-reviewed”]

**Last checked:** [Date]

**Next review due:** [Date or review cycle]

**How to report a problem:** [Issue tracker, email, or other contact]

**Change history:** [Link to Git history, releases, or brief notes]

