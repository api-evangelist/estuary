# Estuary (estuary)

Estuary builds Estuary Flow, a real-time data movement platform for streaming ETL and change data capture (CDC). Flow captures data from databases, warehouses, and SaaS systems into durable collections and materializes those collections back out to destinations. The Flow control plane exposes a Supabase/PostgREST-based REST API (Bearer refresh/access tokens) covering captures, materializations, collections, catalog drafts and publications, connectors, and tenants/billing, while the data plane is driven declaratively via the flowctl CLI and a Gitops model.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/estuary/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/estuary/refs/heads/main/apis.yml)

## Tags

- Data Integration
- Streaming ETL
- Change Data Capture
- CDC
- Real-Time Data
- Data Pipelines

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Estuary Captures API

Manage capture task specifications that continuously ingest data from source databases, warehouses, and SaaS systems into Flow collections, modeled as live_specs of catalogType 'capture' and materialized through the draft and publication workflow.

- **Human URL:** [https://docs.estuary.dev/concepts/captures/](https://docs.estuary.dev/concepts/captures/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Captures
- Ingestion
- CDC

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/captures/)
- [API Reference](https://docs.estuary.dev/concepts/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Materializations API

Manage materialization task specifications that push Flow collections out to destination systems (databases, warehouses, queues), modeled as live_specs of catalogType 'materialization' and published from drafts.

- **Human URL:** [https://docs.estuary.dev/concepts/materialization/](https://docs.estuary.dev/concepts/materialization/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Materializations
- Destinations
- Sync

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/materialization/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Collections API

Read and manage collections - durable, schematized, real-time datasets of JSON documents keyed and stored in cloud object storage - exposed as live_specs of catalogType 'collection' with their JSON Schema and key.

- **Human URL:** [https://docs.estuary.dev/concepts/collections/](https://docs.estuary.dev/concepts/collections/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Collections
- Schemas
- Storage

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/collections/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Catalog Drafts API

Create and edit drafts and their draft_specs - the staging area where proposed changes to captures, materializations, and collections are assembled and tested before being published into the live catalog.

- **Human URL:** [https://docs.estuary.dev/concepts/catalogs/](https://docs.estuary.dev/concepts/catalogs/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Drafts
- Catalog
- Specs

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/catalogs/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Publications API

Submit a draft for publication, validating and promoting its specs into the running data plane as live_specs; asynchronous jobs recorded in the publications table with a job status polled until completion.

- **Human URL:** [https://docs.estuary.dev/concepts/catalogs/](https://docs.estuary.dev/concepts/catalogs/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Publications
- Publish
- Catalog

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/catalogs/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Connectors API

Browse the catalog of available capture and materialization connectors and their tagged image versions (connectors, connector_tags), and run schema discovery against a configured connector via the discovers surface.

- **Human URL:** [https://docs.estuary.dev/concepts/connectors/](https://docs.estuary.dev/concepts/connectors/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Connectors
- Catalog
- Discovery

#### Properties

- [Documentation](https://docs.estuary.dev/concepts/connectors/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Tenants & Billing API

Read tenant configuration, catalog usage statistics (catalog_stats - bytes and docs captured/materialized), and monthly billing estimates via the billing_report_202308 RPC used to meter data-movement GB and connector instances.

- **Human URL:** [https://docs.estuary.dev/getting-started/pricing/](https://docs.estuary.dev/getting-started/pricing/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Tenants
- Billing
- Usage

#### Properties

- [Documentation](https://docs.estuary.dev/getting-started/pricing/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Estuary Auth & Tokens API

Manage long-lived refresh_tokens and exchange a refresh token for a short-lived access token via the generate_access_token RPC; inspect roles and capability grants (user_grants, role_grants) that authorize catalog access.

- **Human URL:** [https://docs.estuary.dev/reference/authentication/](https://docs.estuary.dev/reference/authentication/)
- **Base URL:** `https://api.estuary.dev`

#### Tags

- Authentication
- Tokens
- Access Control

#### Properties

- [Documentation](https://docs.estuary.dev/reference/authentication/)
- [OpenAPI](openapi/estuary-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/estuary.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/estuary.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/estuary)
- [LinkedIn](https://www.linkedin.com/company/estuary-tech)
- [Website](https://estuary.dev/)
- [Documentation](https://docs.estuary.dev)
- [Plans](plans/estuary-plans-pricing.yml)
- [Rate Limits](rate-limits/estuary-rate-limits.yml)
- [Fin Ops](finops/estuary-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
