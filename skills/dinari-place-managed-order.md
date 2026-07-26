---
name: Place a managed dShare order
description: Look up a tradable stock, check its price, place a managed market or limit buy/sell order, and track fulfillment.
api: openapi/dinari-openapi-original.yml
operations: [getStocks, getStockCurrentPrice, createMarketBuyManagedOrderRequest, createLimitBuyManagedOrderRequest, getOrderRequestById, getOrders, getAccountOrderFulfillments]
---

# Place a managed dShare order

Managed orders let Dinari custody and execute on the customer's behalf. Requires an
onboarded `account_id` (see dinari-onboard-entity). Send `X-API-Key-Id` +
`X-API-Secret-Key` on every call.

## Steps

1. **Find the asset** — `getStocks` (GET `/api/v2/market_data/stocks/`) to resolve a
   `stock_id`. Set `limit` to use cursor pagination.
2. **Check price** — `getStockCurrentPrice` (GET `/api/v2/market_data/stocks/{stock_id}/current_price`).
3. **Place the order**:
   - Market buy: `createMarketBuyManagedOrderRequest`
     (POST `/api/v2/accounts/{account_id}/order_requests/market_buy`). Optionally set
     `payment_token_address` to opt out of default USD+ payment.
   - Limit buy: `createLimitBuyManagedOrderRequest` (`.../limit_buy`).
   Capture the returned `order_request_id`.
4. **Track it** — `getOrderRequestById` until it resolves to an order, then `getOrders`
   and `getAccountOrderFulfillments` (GET `/api/v2/accounts/{account_id}/order_fulfillments`)
   for fills.

## Rules

- 423 Locked means the order/account is temporarily locked — back off and retry later.
- No idempotency key: capture `order_request_id` from the response and reconcile with
  `getListOrderRequests` before re-submitting to avoid duplicate orders.
- Optionally subscribe to `order_data` over WebSocket (asyncapi/dinari-streaming-asyncapi.yml)
  instead of polling.
