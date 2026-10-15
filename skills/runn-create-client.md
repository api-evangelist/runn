---
name: runn-create-client
description: Create a new client and retrieve its details.
api: openapi/runn-openapi.json
operations:
- createClient
- getClient
generated: '2026-10-14'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/runn-openapi.json ; every operationId checked against the contract
---

# runn-create-client

Create a new client and retrieve its details.

## Steps

1. 1. Use `createClient` with the required client fields in the request body.
2. 2. Use `getClient` with the `clientId` returned from the previous step to fetch the created client.

## Rules

- Include an `Authorization: Bearer <token>` header (bearerAuth).
- Rate limit: maximum 120 requests per minute; exceeding returns HTTP 429.
- Pagination parameters `limit` and `cursor` apply to list operations (not used in this task).
