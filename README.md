# Marine Data AI Resources

This community project helps people and AI agents discover, access, interpret, and responsibly use marine data facilities.

In this project, a **data facility** is an organization, program, or independently operated service that curates, manages, or provides access to marine data. We use **repository** for this GitHub project and other source-code repositories.

The project is developing:

- a catalog of self-contained profiles describing marine data facilities;
- a shared template for creating those profiles; and
- tested guidance and skills for common marine-data tasks, added as they are developed.

Facility profiles explain what a facility contains, when it should be used, which information it is authoritative for, and which access methods it supports. They can point to official facility documentation, APIs, data services, MCP services, skills, schemas, vocabularies, examples, and related resources.

## Current status

This repository is at an early, community-development stage. Its templates, terminology, and workflows remain open to testing and revision. Draft material should not be described as an adopted ESIP standard.

## Start here

- Browse the [facility catalog](data-facilities/README.md).
- Use the [facility page template](templates/data-facility-profile-template.md) to draft a profile.
- Use or review the project's [agent skills](skills/README.md).
- Read the [contribution guidance](CONTRIBUTING.md) before proposing a change.

When this repository is opened in an agentic development environment, [AGENTS.md](AGENTS.md) provides instructions for working with its contents. Individual facility profiles are also intended to be understandable when supplied to an agent on their own.

## Scope and principles

- Facility owners are the authority on their own systems and services.
- Guidance should distinguish supported, experimental, internal, unadvertised, deprecated, and unavailable interfaces.
- Uncertainty, limitations, and disagreement should be documented rather than hidden.
- Detailed facility documentation should be linked rather than duplicated.
- Guidance should be useful to humans as well as agents.
- Examples and skills should be tested with real marine-data questions.

This project does **not** require facilities to provide an API, MCP server, agent skill, or any other single technical solution. It concerns guidance for agents using data facilities; it is distinct from assessing whether an individual dataset is suitable for AI or machine-learning applications.

## What is an agent skill?

An agent skill is a reusable set of instructions that helps an AI agent perform a particular task using available tools and context. A facility profile provides context about a data facility; a skill provides a workflow for accomplishing a task. Either may link to the other.

Related skill formats and projects include:

- [Agent Skills](https://agentskills.io/)
- [Anthropic Skills](https://github.com/anthropics/skills)
- [Google Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format)

## Project home

This project is maintained through the [ESIP Marine Data Cluster](https://www.esipfed.org/collaboration-areas/marine-data/).
