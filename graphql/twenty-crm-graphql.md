# Twenty GraphQL Schema

Representative GraphQL schema for [Twenty](https://twenty.com/), the open-source CRM.
Twenty auto-generates a GraphQL API alongside its REST API from your workspace data
model. There is no single static schema because each workspace has its own objects and
fields; the schema below is a **representative** view of the standard Core and Metadata
surface and is not a literal export of any one workspace.

- API docs: <https://docs.twenty.com/developers/extend/api>
- Core GraphQL endpoint: `https://api.twenty.com/graphql` (self-hosted: `https://{your-domain}/graphql`)
- Metadata GraphQL endpoint: `https://api.twenty.com/metadata` (self-hosted: `https://{your-domain}/metadata`)
- GitHub: <https://github.com/twentyhq/twenty>

---

## Authentication

Every request is authenticated with a Bearer API key created under Settings -> API & Webhooks:

```
Authorization: Bearer <YOUR_API_KEY>
```

---

## Schema file

See [`twenty-crm-schema.graphql`](./twenty-crm-schema.graphql) for the representative schema.

---

## Surfaces

| Endpoint | Path | Purpose |
|----------|------|---------|
| Core API | `/graphql` | Queries and mutations over CRM records (people, companies, opportunities, notes, tasks, custom objects). |
| Metadata API | `/metadata` | Queries and mutations over schema (objects, fields, relations). |

Both surfaces support cursor-based pagination, filtering, ordering, relation traversal,
and batch operations. Batch upsert mutations use plural object names (for example
`createCompanies`) and accept up to 60 records per request.

---

## Conventions

- **Connections**: list queries return Relay-style connections with `edges { node }`,
  `pageInfo`, and `totalCount`.
- **Filtering**: list queries accept a `filter` input object with per-field comparators
  (`eq`, `in`, `gt`, `lt`, `like`, etc.).
- **Ordering**: list queries accept an `orderBy` argument referencing fields and direction.
- **Composite fields**: rich types such as `FullName`, `Emails`, `Phones`, `Links`, and
  `Currency` are modeled as nested objects, matching the REST representation.

---

## Query examples

### List companies

```graphql
query {
  companies(first: 30, orderBy: { createdAt: DescNullsLast }) {
    edges {
      node {
        id
        name
        employees
        domainName { primaryLinkUrl }
      }
    }
    pageInfo { hasNextPage endCursor }
    totalCount
  }
}
```

### Fetch a person with their company

```graphql
query {
  person(filter: { id: { eq: "00000000-0000-0000-0000-000000000000" } }) {
    id
    name { firstName lastName }
    emails { primaryEmail }
    jobTitle
    company {
      id
      name
    }
  }
}
```

### Create an opportunity

```graphql
mutation {
  createOpportunity(
    data: {
      name: "Acme - Platform Deal"
      stage: PROPOSAL
      amount: { amountMicros: 25000000000, currencyCode: "USD" }
      companyId: "00000000-0000-0000-0000-000000000000"
    }
  ) {
    id
    name
    stage
  }
}
```

### Batch create people (plural / batch upsert)

```graphql
mutation {
  createPeople(
    data: [
      { name: { firstName: "Ada", lastName: "Lovelace" } }
      { name: { firstName: "Alan", lastName: "Turing" } }
    ]
  ) {
    id
    name { firstName lastName }
  }
}
```

### Create a custom object (Metadata API)

```graphql
mutation {
  createOneObject(
    input: {
      object: {
        nameSingular: "project"
        namePlural: "projects"
        labelSingular: "Project"
        labelPlural: "Projects"
        icon: "IconBriefcase"
      }
    }
  ) {
    id
    nameSingular
    namePlural
  }
}
```

### Add a field to an object (Metadata API)

```graphql
mutation {
  createOneField(
    input: {
      field: {
        name: "budget"
        label: "Budget"
        type: CURRENCY
        objectMetadataId: "00000000-0000-0000-0000-000000000000"
      }
    }
  ) {
    id
    name
    type
  }
}
```
