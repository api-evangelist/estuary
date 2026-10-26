# Estuary (estuary)

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
