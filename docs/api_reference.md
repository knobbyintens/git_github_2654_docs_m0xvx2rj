# Northwind Payments API Reference

## Authentication

Every request must include an `Authorization: Bearer <token>` header. API tokens are issued from the merchant dashboard.

## Rate limits

Each API key is allowed to send 1200 requests per minute across all endpoints. The limit is enforced by the edge gateway. When the limit is exceeded the API responds with HTTP 429 and a `Retry-After` header. Short bursts of up to 1800 requests are allowed for 10 seconds under the "burst smoothing" policy.

## Refunds

`POST /v2/refunds` creates a refund for a captured payment. Refund requests are idempotent when a unique `Idempotency-Key` header is provided.

## Webhooks

Webhook deliveries are retried for up to 24 hours. Receivers must acknowledge each delivery within 10 seconds.
