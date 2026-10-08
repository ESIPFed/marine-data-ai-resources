# Contributing to Marine Data AI Resources

Thank you for contributing. This is a community project of the ESIP Marine Data Cluster, and contributions from data facilities, data users, domain experts, and agent-tool developers are welcome.

All participants must follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Ways to contribute

You can:

- create or improve a marine data facility profile;
- test a profile using a real data-discovery or access question;
- report an unclear instruction, incorrect claim, broken link, or missing facility;
- propose a reusable skill or example after its workflow has been tested; or
- contribute relevant standards, tools, and related community work.

## Contributing a facility profile

1. Copy [the facility page template](templates/data-facility-profile-template.md) to `data-facilities/<short-name>.md`.
2. Complete all required **Core** sections.
3. Keep only the interchangeable access modules and optional sections that apply.
4. Cite authoritative sources, preferably official facility documentation, for factual claims and access instructions.
5. Clearly distinguish supported services from experimental, internal, unadvertised, deprecated, or community-developed resources.
6. Identify who prepared the profile, whether a facility representative reviewed it, and when its links and instructions were last checked.
7. Remove template comments, placeholders, and empty sections.
8. Add the profile to the catalog in `data-facilities/README.md`.

A profile does not need to describe an API, MCP server, skill, or every possible access method. It should accurately document what the facility can sustainably support.

## Review expectations

Contributors and reviewers should check that:

- the profile does not overstate the facility's scope or authority;
- identifiers and relationships are described without hiding ambiguity;
- preferred access paths and safe failure behavior are clear;
- provenance, versions, citation, and known limitations are addressed;
- links and examples work as described; and
- the recorded review status is accurate.

Facility review is encouraged but is not required for an initial community-contributed draft. The profile must not imply facility endorsement until a named representative has reviewed it.

## Proposing a change

Fork the repository, create a focused branch, make the change, and submit a pull request. Keep each pull request limited to one coherent profile or project change whenever practical. Use the pull-request description to identify sources, testing performed, unresolved questions, and requested reviewers.

For help with pull requests, see [GitHub's pull-request documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork).
