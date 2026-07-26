---
name: Connect a wallet and fund a Dinari account
description: Connect a customer's blockchain wallet to their account, fund a sandbox account via the faucet, and read the portfolio and cash balance.
api: openapi/dinari-openapi-original.yml
operations: [getAccountWalletConnectionNonce, createAccountWalletConnection, createAccountWalletInternalConnection, createAccountFaucet, getAccountPortfolio, getAccountCash, getWallet]
---

# Connect a wallet and fund a Dinari account

Dinari settles dShares on-chain, so accounts connect to blockchain wallets. Requires an
`account_id`. Send `X-API-Key-Id` + `X-API-Secret-Key` on every call.

## Steps

1. **Get a connection nonce** — `getAccountWalletConnectionNonce`
   (GET `/api/v2/accounts/{account_id}/wallet/connect/nonce`). The customer signs it.
2. **Connect the wallet**:
   - External wallet: `createAccountWalletConnection` (POST `.../wallet/connect`) with the
     signed nonce.
   - Dinari-managed/internal wallet: `createAccountWalletInternalConnection`
     (POST `.../wallet/internal`).
   Confirm with `getWallet` (GET `/api/v2/accounts/{account_id}/wallet`).
3. **Fund (sandbox only)** — `createAccountFaucet` (POST `/api/v2/accounts/{account_id}/faucet`)
   to mint test funds so orders can be placed without real money.
4. **Read balances** — `getAccountCash` (GET `.../cash`) and `getAccountPortfolio`
   (GET `.../portfolio`).

## Rules

- The faucet is sandbox-only; in production fund via wallet transfers / withdrawals.
- Errors use the `BaseOpenApiError` envelope; log `error_id`.
- Supported chains include Arbitrum One, HyperEVM, and Avalanche C-Chain (see changelog).
