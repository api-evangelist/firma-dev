---
name: firma-dev-create-and-test-webhook
description: Create a new webhook and verify it works by sending a test payload.
api: openapi/app_firma_dev_openapi.json
operations:
- createWebhook
- testWebhook
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/app_firma_dev_openapi.json ; every operationId checked against the contract
---

# firma-dev-create-and-test-webhook

Create a new webhook and verify it works by sending a test payload.

## Steps

1. 1. Use `createWebhook` with the required request body fields for the webhook definition.
2. 2. Use `testWebhook` with the webhook `id` returned from the previous step; include any required headers shown in the contract.

## Rules

- Auth: Include an `Authorization` header with the API key (ApiKeyAuth).
- Idempotency: The `createWebhook` operation supports an Idempotency-Key header to avoid duplicate creations.
