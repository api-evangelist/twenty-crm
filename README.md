# Twenty (twenty-crm)

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
