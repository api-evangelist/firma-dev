---
name: firma-dev-create-workspace-with-logo
description: Create a new workspace and upload its logo.
api: openapi/app_firma_dev_openapi.json
operations:
- createWorkspace
- uploadWorkspaceLogo
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/app_firma_dev_openapi.json ; every operationId checked against the contract
---

# firma-dev-create-workspace-with-logo

Create a new workspace and upload its logo.

## Steps

1. 1. Call `createWorkspace` with the request body fields required to define the workspace.
2. 2. Call `uploadWorkspaceLogo` with the path parameter `id` from the created workspace and the multipart/form-data field for the logo file.

## Rules

- Auth: Include the API key in the `Authorization` header as defined by the `ApiKeyAuth` scheme.
- Idempotency: POST requests (`createWorkspace`, `uploadWorkspaceLogo`) should be safe to retry; include an `Idempotency-Key` header if supported.
