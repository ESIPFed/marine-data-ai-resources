# Instructions for AI Agents

## Purpose

This repository is a community-developed catalog of guidance for discovering, accessing, interpreting, and responsibly using marine data facilities.

Do not conflate facility guidance for agents with an assessment of whether individual datasets are AI-ready. Do not assume that every facility should provide an API, MCP server, or agent skill.

## Start here

Before making substantial changes, read:

1. [README.md](README.md) for project scope and principles.
2. [data-facilities/README.md](data-facilities/README.md) for the facility catalog and status terms.
3. [templates/data-facility-profile-template.md](templates/data-facility-profile-template.md) when creating or revising a facility profile.
4. [CONTRIBUTING.md](CONTRIBUTING.md) for contribution requirements.

## Using facility profiles

When helping with a marine-data question:

1. Clarify the relevant place, time, platform or cruise, observed properties, product type, and desired output when they are not already clear.
2. Identify potentially relevant facility profiles in the catalog.
3. Use each profile to understand facility scope, authority, identifiers, access paths, limitations, and related facilities.
4. Follow links to authoritative official facility documentation when current or detailed information is needed.
5. Distinguish documented facts from inferences, and report uncertainty rather than inventing missing information.
6. Preserve provenance by reporting the source facility, relevant identifiers, product version or status, and supporting links.

## Creating or revising a facility profile

1. Copy the template to `data-facilities/<short-name>.md` using a clear lowercase filename.
2. Complete every required **Core** section.
3. Keep, remove, or reorder the interchangeable access modules to match the facility's actual capabilities.
4. Prefer authoritative, official facility sources and links over copied explanations.
5. Clearly label unsupported, experimental, internal, unadvertised, deprecated, or uncertain information.
6. Record the profile's preparer, review status, sources, and review date.
7. Remove template comments, placeholders, and unused optional sections before proposing publication.
8. Add or update the corresponding entry in `data-facilities/README.md`.

Do not invent facility scope, authority, identifiers, relationships, interfaces, or policies. A community-contributed profile may be useful without implying that the facility has reviewed or endorsed it.

## Current project state

This project is at an early stage. Treat its structure, terminology, templates, and workflows as open to community testing and revision, not as adopted ESIP standards.
