# Cockroach Labs

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

**Areas:** Cluster Management · Cloud · Database · Distributed SQL · Infrastructure · PostgreSQL Compatible · SQL

## Cockroach Labs on APIs.io

Everything profiled for Cockroach Labs is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cockroach-labs/](https://apis.io/providers/cockroach-labs/)** — or go straight to one of the APIs or properties below.

### APIs (45)

- [Cockroach Labs Auth API](https://apis.io/apis/cockroach-labs/cockroach-labs-auth-api/) — Authenticate to the Cluster API by creating and terminating API sessions. Session tokens are passed via the X-Cockroach-API-Session header on subsequent…
- [Cockroach Labs Billing API](https://apis.io/apis/cockroach-labs/cockroach-labs-billing-api/) — Retrieve invoices and billing information for the CockroachDB Cloud organization.
- [Cockroach Labs Clusters API](https://apis.io/apis/cockroach-labs/cockroach-labs-clusters-api/) — Create, list, retrieve, update, and delete CockroachDB Serverless and Dedicated clusters within an organization.
- [Cockroach Labs CMEK API](https://apis.io/apis/cockroach-labs/cockroach-labs-cmek-api/) — Manage customer-managed encryption keys (CMEK) for encrypting cluster data at rest using customer-controlled keys.
- [Cockroach Labs Databases API](https://apis.io/apis/cockroach-labs/cockroach-labs-databases-api/) — Manage databases within a CockroachDB cluster, including creation, listing, updating, and deletion.
- [Cockroach Labs EgressRules API](https://apis.io/apis/cockroach-labs/cockroach-labs-egressrules-api/) — Configure egress traffic rules and egress private endpoints for outbound cluster network traffic.
- [Cockroach Labs Folders API](https://apis.io/apis/cockroach-labs/cockroach-labs-folders-api/) — Organize clusters and other resources into hierarchical folder structures within the organization.
- [Cockroach Labs Health API](https://apis.io/apis/cockroach-labs/cockroach-labs-health-api/) — Check the health and readiness of individual CockroachDB nodes. The health endpoint can report whether the node is live and fully operational for accepting…
- [Cockroach Labs IPAllowlists API](https://apis.io/apis/cockroach-labs/cockroach-labs-ipallowlists-api/) — Configure IP allowlist entries to control network access to a cluster.
- [Cockroach Labs JWTIssuers API](https://apis.io/apis/cockroach-labs/cockroach-labs-jwtissuers-api/) — Manage JWT issuer configurations for external identity provider integrations.
- [Cockroach Labs LogExport API](https://apis.io/apis/cockroach-labs/cockroach-labs-logexport-api/) — Configure log export to external destinations such as AWS CloudWatch or GCP Cloud Logging.
- [Cockroach Labs MetricExport API](https://apis.io/apis/cockroach-labs/cockroach-labs-metricexport-api/) — Configure metric export integrations including AWS CloudWatch, Datadog, and Prometheus.
- [Cockroach Labs Nodes API](https://apis.io/apis/cockroach-labs/cockroach-labs-nodes-api/) — Retrieve information about all nodes in the cluster, including their status, address, locality, and operational metrics.
- [Cockroach Labs Organizations API](https://apis.io/apis/cockroach-labs/cockroach-labs-organizations-api/) — Retrieve information about the caller's CockroachDB Cloud organization.
- [Cockroach Labs Ranges API](https://apis.io/apis/cockroach-labs/cockroach-labs-ranges-api/) — List and inspect range information for the cluster, including hot ranges by node and detailed information for specific range IDs.
- [Cockroach Labs Rules API](https://apis.io/apis/cockroach-labs/cockroach-labs-rules-api/) — Retrieve alerting rules templates for use with Prometheus-compatible alerting systems.
- [Cockroach Labs Sessions API](https://apis.io/apis/cockroach-labs/cockroach-labs-sessions-api/) — List active SQL sessions across all nodes of the cluster, with optional filtering by username.
- [Cockroach Labs SQLUsers API](https://apis.io/apis/cockroach-labs/cockroach-labs-sqlusers-api/) — Manage SQL users for a cluster, including creating users, listing users, and updating SQL user passwords.
- [Cockroach Labs VersionDeferral API](https://apis.io/apis/cockroach-labs/cockroach-labs-versiondeferral-api/) — Manage cluster version deferral policies to delay automatic CockroachDB version upgrades.
- [Cockroach Labs API Keys API](https://apis.io/apis/cockroach-labs/cockroach-labs-api-keys-api/) — Manage API keys for programmatic access, including creation, retrieval, listing, updating, and deletion.
- [Cockroach Labs Audit Logs API](https://apis.io/apis/cockroach-labs/cockroach-labs-audit-logs-api/) — Retrieve audit log events for the organization to support compliance and security investigations.
- [Cockroach Labs Backup Restore API](https://apis.io/apis/cockroach-labs/cockroach-labs-backup-restore-api/) — Manage cluster backups, backup configurations, and restore operations for CockroachDB clusters.
- [Cockroach Labs Maintenance Windows API](https://apis.io/apis/cockroach-labs/cockroach-labs-maintenance-windows-api/) — Configure maintenance windows and blackout periods for cluster upgrade scheduling.
- [Cockroach Labs Role Management API](https://apis.io/apis/cockroach-labs/cockroach-labs-role-management-api/) — Manage role-based access control, including assigning and removing roles for users across organization, folder, and cluster scopes.
- [Cockroach Labs Service Accounts API](https://apis.io/apis/cockroach-labs/cockroach-labs-service-accounts-api/) — Manage service accounts used for machine-to-machine authentication within the organization.
- [Cockroach Labs Blackout Windows API](https://apis.io/apis/cockroach-labs/cockroach-labs-blackout-windows-api/) — The Blackout Windows API from Cockroach Labs — 2 operation(s) for blackout windows.
- [Cockroach Labs Client CA Certificates API](https://apis.io/apis/cockroach-labs/cockroach-labs-client-ca-certificates-api/) — The Client CA Certificates API from Cockroach Labs — 1 operation(s) for client ca certificates.
- [Cockroach Labs Cluster Disruption API](https://apis.io/apis/cockroach-labs/cockroach-labs-cluster-disruption-api/) — The Cluster Disruption API from Cockroach Labs — 1 operation(s) for cluster disruption.
- [Cockroach Labs Customer-managed Encryption Keys API](https://apis.io/apis/cockroach-labs/cockroach-labs-customer-managed-encryption-keys-api/) — The Customer-managed Encryption Keys API from Cockroach Labs — 1 operation(s) for customer-managed encryption keys.
- [Cockroach Labs Egress Private Endpoints API](https://apis.io/apis/cockroach-labs/cockroach-labs-egress-private-endpoints-api/) — The Egress Private Endpoints API from Cockroach Labs — 3 operation(s) for egress private endpoints.
- [Cockroach Labs Egress Rules API](https://apis.io/apis/cockroach-labs/cockroach-labs-egress-rules-api/) — The Egress Rules API from Cockroach Labs — 3 operation(s) for egress rules.
- [Cockroach Labs IP Allowlists API](https://apis.io/apis/cockroach-labs/cockroach-labs-ip-allowlists-api/) — The IP Allowlists API from Cockroach Labs — 2 operation(s) for ip allowlists.
- [Cockroach Labs JWT Issuers API](https://apis.io/apis/cockroach-labs/cockroach-labs-jwt-issuers-api/) — The JWT Issuers API from Cockroach Labs — 2 operation(s) for jwt issuers.
- [Cockroach Labs Log Export API](https://apis.io/apis/cockroach-labs/cockroach-labs-log-export-api/) — The Log Export API from Cockroach Labs — 1 operation(s) for log export.
- [Cockroach Labs Metric Export API](https://apis.io/apis/cockroach-labs/cockroach-labs-metric-export-api/) — The Metric Export API from Cockroach Labs — 3 operation(s) for metric export.
- [Cockroach Labs Migration Assistant API](https://apis.io/apis/cockroach-labs/cockroach-labs-migration-assistant-api/) — The Migration Assistant API from Cockroach Labs — 2 operation(s) for migration assistant.
- [Cockroach Labs Physical Cluster Replication API](https://apis.io/apis/cockroach-labs/cockroach-labs-physical-cluster-replication-api/) — The Physical Cluster Replication API from Cockroach Labs — 2 operation(s) for physical cluster replication.
- [Cockroach Labs Private Endpoint Services API](https://apis.io/apis/cockroach-labs/cockroach-labs-private-endpoint-services-api/) — The Private Endpoint Services API from Cockroach Labs — 7 operation(s) for private endpoint services.
- [Cockroach Labs Runtime Scanning API](https://apis.io/apis/cockroach-labs/cockroach-labs-runtime-scanning-api/) — The Runtime Scanning API from Cockroach Labs — 1 operation(s) for runtime scanning.
- [Cockroach Labs SCIM API](https://apis.io/apis/cockroach-labs/cockroach-labs-scim-api/) — The SCIM API from Cockroach Labs — 13 operation(s) for scim.
- [Cockroach Labs SQL Users API](https://apis.io/apis/cockroach-labs/cockroach-labs-sql-users-api/) — The SQL Users API from Cockroach Labs — 3 operation(s) for sql users.
- [Cockroach Labs Version Deferral API](https://apis.io/apis/cockroach-labs/cockroach-labs-version-deferral-api/) — The Version Deferral API from Cockroach Labs — 1 operation(s) for version deferral.
- [Cockroach Labs Virtual Cluster Workspaces API](https://apis.io/apis/cockroach-labs/cockroach-labs-virtual-cluster-workspaces-api/) — The Virtual Cluster Workspaces API from Cockroach Labs — 4 operation(s) for virtual cluster workspaces.
- [Cockroach Labs Private Endpoints API](https://apis.io/apis/cockroach-labs/cockroach-labs-private-endpoints-api/) — Manage private endpoint services and connections for secure VPC-level access to clusters.
- [Cockroach Labs CockroachDB CHANGEFEED Sinks](https://apis.io/apis/cockroach-labs/cockroach-labs-changefeed-sinks/) — Event-driven description of CockroachDB Enterprise CHANGEFEED INTO sinks (Kafka, Google Cloud Pub/Sub, webhook) streaming row-level change data, modeled…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [CockroachDB CHANGEFEED Sinks](https://apis.io/asyncapis/cockroach-labs/cockroach-labs-changefeed-asyncapi/)

#### Event channels (3)

Individual events and webhooks the provider emits.

- [resolved](https://apis.io/channels/cockroach-labs/resolved/)
- [table/{tableName}](https://apis.io/channels/cockroach-labs/table-tablename/)
- [webhook/batch](https://apis.io/channels/cockroach-labs/webhook-batch/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [cockroach-labs-mcp.yml](https://apis.io/servers/cockroach-labs/cockroach-labs-mcp-yml/)

#### Agent skills (33)

Agent skills built on the API.

- [analyzing-range-distribution](https://apis.io/agent-skills/cockroach-labs/analyzing-range-distribution/)
- [analyzing-schema-change-storage-risk](https://apis.io/agent-skills/cockroach-labs/analyzing-schema-change-storage-risk/)
- [auditing-cloud-cluster-security](https://apis.io/agent-skills/cockroach-labs/auditing-cloud-cluster-security/)
- [auditing-table-statistics](https://apis.io/agent-skills/cockroach-labs/auditing-table-statistics/)
- [benchmarking-transaction-patterns](https://apis.io/agent-skills/cockroach-labs/benchmarking-transaction-patterns/)
- [cockroachdb-sql](https://apis.io/agent-skills/cockroach-labs/cockroachdb-sql/)
- [configuring-audit-logging](https://apis.io/agent-skills/cockroach-labs/configuring-audit-logging/)
- [configuring-ip-allowlists](https://apis.io/agent-skills/cockroach-labs/configuring-ip-allowlists/)
- [configuring-log-export](https://apis.io/agent-skills/cockroach-labs/configuring-log-export/)
- [configuring-private-connectivity](https://apis.io/agent-skills/cockroach-labs/configuring-private-connectivity/)
- [configuring-sso-and-scim](https://apis.io/agent-skills/cockroach-labs/configuring-sso-and-scim/)
- [designing-application-transactions](https://apis.io/agent-skills/cockroach-labs/designing-application-transactions/)
- [designing-multi-region-applications](https://apis.io/agent-skills/cockroach-labs/designing-multi-region-applications/)
- [enabling-cmek-encryption](https://apis.io/agent-skills/cockroach-labs/enabling-cmek-encryption/)
- [enforcing-password-policies](https://apis.io/agent-skills/cockroach-labs/enforcing-password-policies/)
- [hardening-user-privileges](https://apis.io/agent-skills/cockroach-labs/hardening-user-privileges/)
- [managing-certificates-and-encryption](https://apis.io/agent-skills/cockroach-labs/managing-certificates-and-encryption/)
- [managing-cluster-capacity](https://apis.io/agent-skills/cockroach-labs/managing-cluster-capacity/)
- [managing-cluster-settings](https://apis.io/agent-skills/cockroach-labs/managing-cluster-settings/)
- [managing-tls-certificates](https://apis.io/agent-skills/cockroach-labs/managing-tls-certificates/)
- [molt-fetch](https://apis.io/agent-skills/cockroach-labs/molt-fetch/)
- [molt-replicator](https://apis.io/agent-skills/cockroach-labs/molt-replicator/)
- [molt-verify](https://apis.io/agent-skills/cockroach-labs/molt-verify/)
- [monitoring-background-jobs](https://apis.io/agent-skills/cockroach-labs/monitoring-background-jobs/)
- [performing-cluster-maintenance](https://apis.io/agent-skills/cockroach-labs/performing-cluster-maintenance/)
- …and 8 more published on APIs.io

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cockroach Labs Agentic Access](https://apis.io/agentic-access/cockroach-labs/cockroach-labs-agentic-access/)

#### JSON Schema (73)

The data models the API reads and writes.

- [AddEgressRuleRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-add-egress-rule-request/)
- [AddJWTIssuerRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-add-jwtissuer-request/)
- [AddPrivateEndpointConnectionRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-add-private-endpoint-connection-request/)
- [AllowlistEntry](https://apis.io/schemas/cockroach-labs/cockroach-labs-allowlist-entry/)
- [ApiKey](https://apis.io/schemas/cockroach-labs/cockroach-labs-api-key/)
- [BackupConfiguration](https://apis.io/schemas/cockroach-labs/cockroach-labs-backup-configuration/)
- [CloudWatchMetricExportInfo](https://apis.io/schemas/cockroach-labs/cockroach-labs-cloud-watch-metric-export-info/)
- [CockroachDB Cluster](https://apis.io/schemas/cockroach-labs/cockroach-labs-cluster/)
- [ClusterVersionDeferral](https://apis.io/schemas/cockroach-labs/cockroach-labs-cluster-version-deferral/)
- [CMEKClusterInfo](https://apis.io/schemas/cockroach-labs/cockroach-labs-cmekcluster-info/)
- [CMEKClusterSpecification](https://apis.io/schemas/cockroach-labs/cockroach-labs-cmekcluster-specification/)
- [CreateApiKeyRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-api-key-request/)
- [CreateApiKeyResponse](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-api-key-response/)
- [CreateClusterRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-cluster-request/)
- [CreateDatabaseRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-database-request/)
- [CreateFolderRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-folder-request/)
- [CreateServiceAccountRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-service-account-request/)
- [CreateSQLUserRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-create-sqluser-request/)
- [Database](https://apis.io/schemas/cockroach-labs/cockroach-labs-database/)
- [DatadogMetricExportInfo](https://apis.io/schemas/cockroach-labs/cockroach-labs-datadog-metric-export-info/)
- [EditEgressRuleRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-edit-egress-rule-request/)
- [EgressRule](https://apis.io/schemas/cockroach-labs/cockroach-labs-egress-rule/)
- [EnableCloudWatchMetricExportRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-enable-cloud-watch-metric-export-request/)
- [EnableDatadogMetricExportRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-enable-datadog-metric-export-request/)
- [EnableLogExportRequest](https://apis.io/schemas/cockroach-labs/cockroach-labs-enable-log-export-request/)
- …and 48 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Cockroach Labs Context](https://apis.io/jsonld/cockroach-labs/cockroach-labs-context/)

#### Collections (54)

Postman and Open Collection request collections.

- [CockroachDB Cloud APIKeys API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-apikeys-api/)
- [CockroachDB Cloud APIKeys AuditLogs API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-auditlogs-api/)
- [CockroachDB Cloud APIKeys Auth API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-auth-api/)
- [CockroachDB Cloud APIKeys BackupRestore API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-backuprestore-api/)
- [CockroachDB Cloud APIKeys Billing API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-billing-api/)
- [CockroachDB Cloud API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-cloud-api/)
- [CockroachDB Cluster API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-cluster-api/)
- [CockroachDB Cloud APIKeys Clusters API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-clusters-api/)
- [CockroachDB Cloud APIKeys CMEK API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-cmek-api/)
- [CockroachDB Cloud APIKeys Databases API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-databases-api/)
- [CockroachDB Cloud APIKeys EgressRules API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-egressrules-api/)
- [CockroachDB Cloud APIKeys Folders API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-folders-api/)
- [CockroachDB Cloud APIKeys Health API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-health-api/)
- [CockroachDB Cloud APIKeys IPAllowlists API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-ipallowlists-api/)
- [CockroachDB Cloud APIKeys JWTIssuers API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-jwtissuers-api/)
- [CockroachDB Cloud APIKeys LogExport API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-logexport-api/)
- [CockroachDB Cloud APIKeys MaintenanceWindows API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-maintenancewindows-api/)
- [CockroachDB Cloud APIKeys MetricExport API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-metricexport-api/)
- [CockroachDB Cloud APIKeys Nodes API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-nodes-api/)
- [CockroachDB Cloud APIKeys Organizations API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-organizations-api/)
- [CockroachDB Cloud APIKeys PrivateEndpoints API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-privateendpoints-api/)
- [CockroachDB Cloud APIKeys Ranges API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-ranges-api/)
- [CockroachDB Cloud APIKeys RoleManagement API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-rolemanagement-api/)
- [CockroachDB Cloud APIKeys Rules API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-rules-api/)
- [CockroachDB Cloud APIKeys ServiceAccounts API](https://apis.io/collections/cockroach-labs/open-cockroach-labs-serviceaccounts-api/)
- …and 29 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Cockroach Labs — jsonschema rules](https://apis.io/rules/cockroach-labs/cockroach-labs-jsonschema-spectral-rules/)
- [Cockroach Labs API Rules](https://apis.io/rules/cockroach-labs/cockroach-labs-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Cockroach Labs Authentication](https://apis.io/security/cockroach-labs/cockroach-labs-authentication/)
- [Cockroach Labs Domain Security](https://apis.io/security/cockroach-labs/cockroach-labs-domain-security/)
- [Cockroach Labs Trust Center](https://apis.io/security/cockroach-labs/cockroach-labs-trust-center/)
- [Cockroach Labs Vulnerability Disclosure](https://apis.io/security/cockroach-labs/cockroach-labs-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cockroach Labs Plans Pricing](https://apis.io/plans/cockroach-labs/cockroach-labs-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cockroach Labs Rate Limits](https://apis.io/rate-limits/cockroach-labs/cockroach-labs-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Cockroach Labs Finops](https://apis.io/finops/cockroach-labs/cockroach-labs-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cockroachlabs.com/)
- [Documentation](https://www.cockroachlabs.com/docs/)
- [Getting started](https://docs.cockroachlabs.com/docs/continuum/tutorial-quickstart)
- [API reference](https://docs.cockroachlabs.com/)
- [Pricing](https://www.cockroachlabs.com/pricing/)
- [Sign up](https://www.cockroachlabs.com/partners/signup/)
- [Support](https://www.cockroachlabs.com/support/)
- [Changelog](https://docs.cockroachlabs.com/docs/releases)
- [Blog](https://www.cockroachlabs.com/blog/)
- [Security](https://www.cockroachlabs.com/security/)
- [Compliance](https://www.cockroachlabs.com/security/)
- [Terms of service](https://www.cockroachlabs.com/cloud-terms-and-conditions/)
- [Privacy policy](https://www.cockroachlabs.com/privacy/)
- [Status](https://status.cockroachlabs.cloud/)

## API Evangelist rating

**Kin Score 71.5** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 81.7 |
| Contract quality | 71.8 |
| Contract governance | 22.0 |
| Operational transparency | 55.3 |
| Developer ergonomics | 67.3 |
| Access clarity | 68.4 |

**Agent readiness 43.4** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | verified |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | mostly |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cockroach-labs/](https://apis.io/providers/cockroach-labs/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cockroach Labs: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cockroach-labs/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
