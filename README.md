# Cockroach Labs (cockroach-labs)

Cockroach Labs is the New York-based software company that builds CockroachDB, a cloud-native, distributed, PostgreSQL-compatible SQL database. CockroachDB is offered as Cockroach Labs' fully managed cloud service (Basic, Standard, and Advanced plans) and as self-hosted software. The company provides two primary developer APIs: the CockroachDB Cloud API for managing the lifecycle of cloud-hosted clusters, and the CockroachDB Cluster API exposed by every node for cluster health, monitoring, and operational status. CockroachDB is used in production by banking, retail, gaming, and media companies including Bose, Hard Rock Digital, DoorDash, and Netflix.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
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
- **Modified:** 2026-04-26

## APIs

### CockroachDB Cloud API
REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning, scaling, deletion, SQL user management, network authorization, customer-managed encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export, SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices, and backup configuration. Authenticated via bearer tokens and rate-limited to 10 requests per second per user.

**Human URL:** [https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api](https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api)

#### Tags

- Cloud, Cluster Management, Database, Infrastructure

#### Properties

- [Documentation](https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api)
- [API Reference](https://www.cockroachlabs.com/docs/api/cloud/v1)
- [OpenAPI](openapi/cockroach-labs-cloud-api-openapi.yml)

### CockroachDB Cluster API
REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session and query introspection, database and table metadata, and event log retrieval. Authentication uses session tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header.

**Human URL:** [https://www.cockroachlabs.com/docs/stable/cluster-api](https://www.cockroachlabs.com/docs/stable/cluster-api)

#### Tags

- Cluster, Database, Monitoring, Nodes, Observability

#### Properties

- [Documentation](https://www.cockroachlabs.com/docs/stable/cluster-api)
- [API Reference](https://www.cockroachlabs.com/docs/api/cluster/v2)
- [OpenAPI](openapi/cockroach-labs-cluster-api-openapi.yml)

## Common Properties

- [Website](https://www.cockroachlabs.com/)
- [Documentation](https://www.cockroachlabs.com/docs/)
- [Pricing](https://www.cockroachlabs.com/pricing/)
- [Blog](https://www.cockroachlabs.com/blog/)
- [Glossary](https://www.cockroachlabs.com/docs/stable/architecture/glossary)
- [Console](https://cockroachlabs.cloud/)
- [Status](https://status.cockroachlabs.cloud/)
- [Support](https://www.cockroachlabs.com/support/)
- [Partners](https://www.cockroachlabs.com/partners/)
- [Security](https://www.cockroachlabs.com/security/)
- [GitHub](https://github.com/cockroachdb)
- [Terraform Provider](https://registry.terraform.io/providers/cockroachdb/cockroach/latest)
- [Privacy Policy](https://www.cockroachlabs.com/privacy/)
- [Terms of Service](https://www.cockroachlabs.com/cloud-terms-and-conditions/)
- [JSON-LD Context](json-ld/cockroach-labs-context.jsonld)
- [Cluster JSON Schema](json-schema/cockroach-labs-cluster-schema.json)
- [Spectral Ruleset](rules/cockroach-labs-rules.yml)
- [Naftiko Capabilities](capabilities/cockroach-labs-capabilities.yml)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
