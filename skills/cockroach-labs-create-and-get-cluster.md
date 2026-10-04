---
name: cockroach-labs-create-and-get-cluster
description: Create a new CockroachDB cluster and retrieve its details.
api: openapi/cockroach-labs-clusters-api-openapi.yml
operations:
- CockroachCloud_CreateCluster
- CockroachCloud_GetCluster
- CockroachCloud_GetConnectionString
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/cockroach-labs-clusters-api-openapi.yml ; every operationId checked against the contract
---

# cockroach-labs-create-and-get-cluster

Create a new CockroachDB cluster and retrieve its details.

## Steps

1. 1. `CockroachCloud_CreateCluster` – body fields: name, cloud_provider, region, tier, version, sql_user, sql_password
2. 2. `CockroachCloud_GetCluster` – path parameter: cluster_id (returned from step 1)
3. 3. `CockroachCloud_GetConnectionString` – path parameter: cluster_id

## Rules

- Auth: include a Bearer token in the `Authorization` header (scheme `Bearer`).
- Idempotency: the `CockroachCloud_CreateCluster` operation is not idempotent; avoid retrying without a new request body.
- Errors: 4xx responses indicate client errors (e.g., invalid parameters), 5xx indicate server errors.
