# Twenty (twenty-crm)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Twenty is an open-source CRM and a modern alternative to Salesforce. It auto-generates both a REST API and a GraphQL API from your workspace data model, exposing a Core API for records (People, Companies, Opportunities, Notes, Tasks, and custom objects) and a Metadata API for schema (objects, fields, and relations). Twenty is free to self-host and available as a managed Twenty Cloud offering.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/twenty-crm/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/twenty-crm/refs/heads/main/apis.yml)

## Tags

- CRM
- Open Source
- Sales
- GraphQL
- REST

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Twenty Core REST API

Auto-generated REST CRUD over CRM records - People, Companies, Opportunities, Notes, Tasks, Workspace Members, Attachments, and any custom objects - under the per-workspace /rest base path, with Bearer API key auth and batch operations up to 60 records.

- **Human URL:** [https://docs.twenty.com/developers/extend/api](https://docs.twenty.com/developers/extend/api)
- **Base URL:** `https://api.twenty.com/rest`

#### Tags

- CRM
- People
- Companies
- Opportunities
- Notes
- Tasks

#### Properties

- [Documentation](https://docs.twenty.com/developers/extend/api)
- [API Reference](https://docs.twenty.com/api-reference/openapi.json)
- [OpenAPI](openapi/twenty-crm-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/twenty-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/twenty-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Twenty Metadata REST API

Schema management REST API to create, modify, and delete objects, fields, and relations under the /rest/metadata base path, so custom data models instantly gain matching Core REST and GraphQL endpoints.

- **Human URL:** [https://docs.twenty.com/developers/extend/api](https://docs.twenty.com/developers/extend/api)
- **Base URL:** `https://api.twenty.com/rest/metadata`

#### Tags

- Metadata
- Schema
- Objects
- Fields

#### Properties

- [Documentation](https://docs.twenty.com/developers/extend/api)
- [API Reference](https://docs.twenty.com/api-reference/openapi.json)
- [OpenAPI](openapi/twenty-crm-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/twenty-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/twenty-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Twenty GraphQL API

Auto-generated GraphQL API over the same workspace schema, exposing queries, mutations, batch upserts via plural object names, and relation traversal for the Core API (/graphql) and Metadata API (/metadata), authenticated with a Bearer API key.

- **Human URL:** [https://docs.twenty.com/developers/extend/api](https://docs.twenty.com/developers/extend/api)
- **Base URL:** `https://api.twenty.com/graphql`

#### Tags

- GraphQL
- CRM
- Metadata

#### Properties

- [Documentation](https://docs.twenty.com/developers/extend/api)
- [API Reference](https://docs.twenty.com/api-reference/openapi.json)
- [GraphQL](graphql/twenty-crm-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [GraphQL Schema](graphql/twenty-crm-schema.graphql) — [GraphQL Specification](https://spec.graphql.org/)

## Common Properties

- [GitHub Organization](https://github.com/twentyhq)
- [LinkedIn](https://www.linkedin.com/company/twenty-crm)
- [Website](https://twenty.com/)
- [Documentation](https://docs.twenty.com/)
- [Plans](plans/twenty-crm-plans-pricing.yml)
- [Rate Limits](rate-limits/twenty-crm-rate-limits.yml)
- [Fin Ops](finops/twenty-crm-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
