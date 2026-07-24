---
name: Manage registered (recurring) queries
description: Create a registered query that runs on a recurring basis, list and inspect registered queries, collect their results, and cancel them.
api: openapi/halo-connect-integrator-openapi.json
operations: [createRegisteredQuery, getRegisteredQueries, getRegisteredQuery, getRegisteredQueryResult, cancelRegisteredQuery]
---

# Manage registered (recurring) queries

Registered queries run on a recurring basis against a site and notify you (via
webhook) when a run completes.

## Steps
1. **Create.** Call `createRegisteredQuery` (`POST /integrator/sites/{siteId}/queries/registered`) with the query definition.
2. **List / inspect.** Call `getRegisteredQueries` (`GET /integrator/sites/{siteId}/queries/registered`) and `getRegisteredQuery` (`GET .../registered/{queryId}`) for details and status.
3. **Collect results.** On a `webhookSource: "registered"` notification (or on a schedule), call `getRegisteredQueryResult` (`GET .../registered/{queryId}/results`).
4. **Cancel.** Call `cancelRegisteredQuery` (`DELETE .../registered/{queryId}`) to stop a registered query.

## Notes
- Verify webhook signatures (`X-Halo-Signature-256`, HMAC-SHA256) and reject timestamps older than 5 minutes. See `asyncapi/halo-connect-webhooks-asyncapi.yml`.
- All operations require `Ocp-Apim-Subscription-Key` and correct environment (stage vs production).
