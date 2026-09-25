---
name: firma-dev-jwt-management-generate-and-revoke-signing-request
description: Generate a JWT token for a signing request and then revoke it when it is no longer needed.
api: openapi/app_firma_dev_openapi.json
operations:
- generateSigningRequestToken
- revokeSigningRequestToken
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/app_firma_dev_openapi.json ; every operationId checked against the contract
---

# firma-dev-jwt-management-generate-and-revoke-signing-request

Generate a JWT token for a signing request and then revoke it when it is no longer needed.

## Steps

1. 1. Call `generateSigningRequestToken` providing the required request body fields (as defined in the contract) and include the `Authorization` header with the API key.
2. 2. Call `revokeSigningRequestToken` providing the token identifier in the request body and include the `Authorization` header with the API key.

## Rules

- Auth header: All requests must include an `Authorization` header containing the API key (ApiKeyAuth).
