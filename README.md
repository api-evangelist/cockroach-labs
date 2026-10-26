# Cockroach Labs (cockroach-labs)

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

Cockroach Labs is the New York-based software company that builds CockroachDB, a cloud-native, distributed, PostgreSQL-compatible SQL database. CockroachDB is offered as Cockroach Labs' fully managed cloud service (Basic, Standard, and Advanced plans) and as self-hosted software. The company provides two primary developer APIs: the CockroachDB Cloud API for managing the lifecycle of cloud-hosted clusters, and the CockroachDB Cluster API exposed by every node for cluster health, monitoring, and operational status. CockroachDB is used in production by banking, retail, gaming, and media companies including Bose, Hard Rock Digital, DoorDash, and Netflix.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Cluster Management
- Cloud
- Database
- Distributed SQL
- Infrastructure
- PostgreSQL Compatible
- SQL

## Timestamps

- **Created:** 2024-11-24
- **Modified:** 2026-05-19

## APIs

### CockroachDB Cloud API

REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning, scaling, deletion, SQL user management, network authorization (IP allowlists, private endpoints), customer-managed encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export, SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices, and backup configuration. Authenticated via bearer tokens and rate-limited to 10 requests per second per user. Also available via the official CockroachDB Cloud Terraform provider.

- **Human URL:** [https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api](https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api)
- **Base URL:** `https://cockroachlabs.cloud`

#### Tags

- Cloud
- Cluster Management
- Database
- Infrastructure

#### Properties

- [Documentation](https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api)
- [API Reference](https://www.cockroachlabs.com/docs/api/cloud/v1)
- [OpenAPI](openapi/cockroach-labs-cloud-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cockroach-labs-cloud-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cockroach-labs-cloud-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CockroachDB Cluster API

REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session and query introspection, database and table metadata, and event log retrieval. Authentication uses session tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header. Self-hosted operators typically front the cluster API with a load balancer or service mesh.

- **Human URL:** [https://www.cockroachlabs.com/docs/stable/cluster-api](https://www.cockroachlabs.com/docs/stable/cluster-api)
- **Base URL:** `https://localhost:8080`

#### Tags

- Cluster
- Database
- Monitoring
- Nodes
- Observability

#### Properties

- [Documentation](https://www.cockroachlabs.com/docs/stable/cluster-api)
- [API Reference](https://www.cockroachlabs.com/docs/api/cluster/v2)
- [OpenAPI](openapi/cockroach-labs-cluster-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cockroach-labs-cluster-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cockroach-labs-cluster-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/cockroach-labs)
- [Website](https://www.cockroachlabs.com/)
- [Documentation](https://www.cockroachlabs.com/docs/)
- [Pricing](https://www.cockroachlabs.com/pricing/)
- [Blog](https://www.cockroachlabs.com/blog/)
- [Glossary](https://www.cockroachlabs.com/docs/stable/architecture/glossary)
- [Console](https://cockroachlabs.cloud/)
- [Status Page](https://status.cockroachlabs.cloud/)
- [Support](https://www.cockroachlabs.com/support/)
- [Partners](https://www.cockroachlabs.com/partners/)
- [Security](https://www.cockroachlabs.com/security/)
- [Git Hub](https://github.com/cockroachdb)
- [Terraform Provider](https://registry.terraform.io/providers/cockroachdb/cockroach/latest)
- [Privacy Policy](https://www.cockroachlabs.com/privacy/)
- [Terms of Service](https://www.cockroachlabs.com/cloud-terms-and-conditions/)
- [JSON-LD](json-ld/cockroach-labs-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/cockroach-labs-cluster-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Spectral Rules](rules/cockroach-labs-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)
- [Integrations](https://www.cockroachlabs.com/partners/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
