---
name: Pair a site and run an immediate query
description: Resolve a practice's Halo GUID, confirm the site is available, then run a synchronous SQL passthrough query and read the result.
api: openapi/halo-connect-integrator-openapi.json
operations: [getSites, Integrator_PairSite, getSite, createImmediateQuery, getResultPage]
---

# Pair a site and run an immediate query

Use the Halo Cloud Integrator API to query an on-premise practice management system.

## Auth
Send `Ocp-Apim-Subscription-Key: <your key>` on every request. Keys are
environment-scoped: production is `https://api.haloconnect.io`, staging is
`https://api.stage.haloconnect.io` — a production key will 401 against staging.

## Steps
1. **Resolve the site.** Call `getSites` (`GET /integrator/sites`) with the PMS ID to exchange it for the practice's Halo GUID (`siteId`).
2. **Pair if needed.** If the site is not yet paired to your integrator, call `Integrator_PairSite` (`POST /integrator/pair-site`). Prefer this over the deprecated `pairSite` (`POST /integrator/pairSite`).
3. **Check availability.** Call `getSite` (`GET /integrator/sites/{siteId}`) and confirm the site status/availability before querying — an offline site returns 503/504 on query.
4. **Run the query.** Call `createImmediateQuery` (`POST /integrator/sites/{siteId}/queries/immediate`). Immediate results are capped at 8MB; a 413 means you must narrow the query or switch to async.
5. **Read results.** If paged, call `getResultPage` (`GET /integrator/sites/{siteId}/queries/{queryId}/results/{pageNumber}`).

## Error handling
- 401 → wrong key or environment. 403 `Caller Ip Not Allowed` → integrator IP not allowlisted (contact support). 413 → results >8MB, use async. 504 → query >30s, use async. See `errors/halo-connect-error-codes.yml`.
- There is no idempotency key; re-submitting creates a new query.
