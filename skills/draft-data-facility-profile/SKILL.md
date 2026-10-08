---
name: draft-data-facility-profile
description: Guide a contributor through researching, drafting, or revising a marine data facility profile using this project's template. Use for facility-profile contributions, not for answering general data-discovery questions.
---

# Draft a Marine Data Facility Profile

Help a contributor produce a useful, traceable profile without requiring them to answer the entire template at once. Treat the profile as contextual guidance, not as a certification of the facility.

## Load the project context

Before drafting, read:

- the [project scope and principles](../../README.md);
- the [facility catalog and status terms](../../data-facilities/README.md);
- the [facility page template](../../templates/data-facility-profile-template.md); and
- the [contribution and review requirements](../../CONTRIBUTING.md).

If revising an existing profile, read it before proposing changes.

## Establish the contribution

At the start of the walkthrough, briefly explain the process and reassure the contributor that they do not need every answer. For example:

> We'll work through the profile in manageable sections. It's fine to say "I don't know" or skip a question. I'll check official documentation where possible, flag anything that needs someone else's input, and keep track of open questions while we continue.

Determine whether the contributor is creating, revising, or reviewing a profile. Establish the facility name, short name, primary website, intended profile status, and likely facility reviewer when known.

Work interactively. Ask compact groups of questions only when the answers materially affect the profile. Do not ask the contributor to transcribe facts that can be verified efficiently from authoritative public documentation.

Separate:

- **verifiable facts**, such as documented holdings, endpoints, file formats, and identifier specifications;
- **facility judgments**, such as authoritative roles, supported interfaces, extraction policies, and service expectations; and
- **community guidance**, such as suggested workflows, cross-facility comparisons, and experimental skills.

Facility judgments should be confirmed by an appropriate representative or marked as awaiting review.

When a contributor does not know an answer:

- Check official documentation for verifiable facts, within the available access and tools.
- If the answer remains unresolved or needs a facility decision, record a specific open question in the working draft, including the relevant source or suggested reviewer when known.
- Continue with sections that do not depend on that answer. Do not repeat the question or require the contributor to guess.

Distinguish "unknown" from "not offered," "unsupported," and "not applicable." At handoff, collect the remaining open questions for review; unresolved questions do not prevent a useful draft, but may prevent treating it as complete.

## Draft in useful passes

### 1. Complete the Core sections

Start with scope, authoritative role, appropriate uses, holdings, effective search inputs, important entities and identifiers, and the recommended discovery and access path.

Resolve these sections before spending time on every possible access mechanism. If an important fact is unresolved, record a specific open question rather than filling the gap with a plausible assumption.

### 2. Select access modules

Keep only modules that describe actual capabilities or important explicit absences. Distinguish technical availability from a supported public service.

For each retained method, establish its status, authoritative documentation, expected inputs and outputs, limitations, and failure behavior. A profile is not deficient merely because the facility does not provide an API, MCP service, or skill.

When a generic service skill exists, such as an ERDDAP skill, link it alongside the facility-specific details needed to apply it correctly. Do not duplicate an externally maintained skill solely to make the central repository appear comprehensive.

### 3. Add interpretation and trust guidance

Document the domain knowledge needed to avoid misuse, including formats, units, quality flags, versions, provenance, citation, known limitations, and cross-facility relationships.

State what an agent should do when evidence is incomplete, identifiers conflict, or an access path fails. Prefer asking, verifying, or stopping over silently substituting data or inventing a relationship.

### 4. Add examples only when they are meaningful

Examples should use realistic questions and identify required clarification, expected evidence, common failures, and safe responses. Label untested examples honestly. Do not present a hypothetical workflow as demonstrated behavior.

### 5. Record ownership and review

Identify who prepared the profile, who reviewed it on behalf of the facility, when sources and links were checked, and how problems can be reported. Apply catalog status terms to the profile itself, not to the overall quality of the facility.

## Use sources carefully

Prefer official facility websites, documentation, schemas, source-code repositories, and policies. Use third-party sources primarily to discover authoritative material or to document an explicitly external relationship.

Verify current URLs and changeable service details before relying on them. Keep supporting links near the claims they substantiate. Do not infer permission to scrape, automate, or use an undocumented interface merely because it is technically accessible.

## Write and review the profile

Create or update `data-facilities/<short-name>.md` from the project template and update the catalog entry. Preserve the template's distinctions between Core, recommended, and optional material, but remove unused modules and drafting instructions from a profile proposed for publication.

A working draft may contain clearly marked open questions. Before describing it as complete, confirm that:

- retained sections contain substantive content rather than placeholders;
- claims and links are traceable to sources;
- unknown, unsupported, and experimental information is labeled accurately;
- access instructions include appropriate limitations and safe failure behavior;
- profile ownership and review status are visible; and
- the facility catalog agrees with the profile.

Summarize unresolved questions and suggested human reviewers when handing off the draft. Do not modify the shared template based on one facility's needs unless the user requests that broader change; instead, record proposed template improvements separately for later comparison across pilots.
