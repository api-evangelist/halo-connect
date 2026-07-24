---
name: Submit an async query and collect results
description: Submit a large or long-running SQL query asynchronously, poll for completion (or receive a webhook), then page through the results.
api: openapi/halo-connect-integrator-openapi.json
operations: [createAsyncQuery, getQuery, getQueryStatusBatch, getResultPage, streamResultPage]
---

# Submit an async query and collect results

Use async queries when results exceed 8MB or a query runs longer than 30 seconds
(both of which fail an immediate query with 413 / 504).

## Steps
1. **Submit.** Call `createAsyncQuery` (`POST /integrator/sites/{siteId}/queries/async`). You receive a `queryId` and a queued status.
2. **Poll status.** Call `getQuery` (`GET /integrator/sites/{siteId}/queries/{queryId}`) until the query reaches a successful (or failed) state. To check many at once, call `getQueryStatusBatch` (`POST /integrator/sites/{siteId}/queries/status`).
3. **Or subscribe to a webhook.** If webhooks are configured for your subscription, Halo POSTs a `webhookSource: "async"` notification with the `queryId` on completion — verify the `X-Halo-Signature-256` HMAC-SHA256 signature and reject timestamps older than 5 minutes. See `asyncapi/halo-connect-webhooks-asyncapi.yml`.
4. **Page the results.** Call `getResultPage` (`GET .../queries/{queryId}/results/{pageNumber}`), or `streamResultPage` (`GET .../queries/{queryId}/results/{pageNumber}/stream`) to stream a page.

## Notes
- Use exponential backoff on 429 (respect `Retry-After`) and on 5xx.
- The webhook payload never contains the result — always fetch it via the API with the `queryId`.
