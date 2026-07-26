---
name: Onboard a Dinari entity (KYC) and open an account
description: Create a customer entity, submit KYC identity and documents, then open a brokerage account ready to trade dShares.
api: openapi/dinari-openapi-original.yml
operations: [createEntities, createEntityKyc, createEntityKycDocument, createManagedEntityKycEmbed, createEntityAccounts, getEntityKyc]
---

# Onboard a Dinari entity and open an account

Use the Dinari Enterprise API to bring a new customer (entity) through KYC and open a
brokerage account. All requests send both `X-API-Key-Id` and `X-API-Secret-Key` headers.
Base URL: `https://api-enterprise.sandbox.dinari.com/api/v2` (sandbox) or
`https://api-enterprise.sbt.dinari.com/api/v2` (live).

## Steps

1. **Create the entity** — `createEntities` (POST `/api/v2/entities`). Capture the returned
   `entity_id` (UUIDv7).
2. **Submit KYC** — either:
   - `createEntityKyc` (POST `/api/v2/entities/{entity_id}/kyc`) to submit identity data
     directly, then `createEntityKycDocument` (POST `.../kyc/document`) to attach documents; or
   - `createManagedEntityKycEmbed` (POST `.../kyc/url`) to hand the customer a hosted/managed
     KYC flow (pass `jurisdiction: US` for managed US KYC).
3. **Confirm KYC status** — poll `getEntityKyc` (GET `/api/v2/entities/{entity_id}/kyc`) until
   the entity is approved.
4. **Open an account** — `createEntityAccounts` (POST `/api/v2/entities/{entity_id}/accounts`).
   Capture `account_id` for all downstream trading and funding.

## Rules

- Errors return the `BaseOpenApiError` envelope (`status`, `message`, `error_id`). Log
  `error_id` for Dinari support. 422 = validation failure; fix the body and retry.
- There is no idempotency-key contract — do not blindly retry POSTs; check state first
  (e.g. `getEntities`) before re-creating.
- Production requires completing KYB with Dinari first (see sandbox/dinari-sandbox.yml).
