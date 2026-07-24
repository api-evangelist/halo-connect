---
name: Search primary-care data with the FHIR R4 API
description: Query a practice's data as FHIR R4 (4.0.1) resources through the Halo Cloud FHIR facade, honoring per-PMS capability.
api: openapi/halo-connect-integrator-openapi.json
operations: [getSite, getFhirQuery, postFhirSearch]
---

# Search primary-care data with the FHIR R4 API

Halo Cloud exposes a FHIR R4 (4.0.1) facade — built toward AU Base 4.1.0 — over
each site's practice management system. It is a facade, not a full FHIR server:
FHIR queries are translated to SQL on the practice database and results are
translated back to FHIR. Supported resources vary per PMS.

## Steps
1. **Confirm capability.** Fetch the CapabilityStatement at `{baseUrl}/metadata` (per-site) to see which resources and operations the PMS supports.
2. **Search (GET).** Call `getFhirQuery` (`GET /integrator/sites/{siteId}/fhir/R4/{fhirParameters}`) for resources such as `Patient`, `Practitioner`, `Appointment`, `DocumentReference`, plus operations like `Patient $summary`, `$waitlist`, `$find-free` where supported.
3. **Search (POST).** For long or complex query strings, call `postFhirSearch` (`POST /integrator/sites/{siteId}/fhir/R4/{resource}/_search`).

## Error handling
- FHIR errors come back as a standard `OperationOutcome` resource (not the general envelope). Inspect `issue[].severity` / `issue[].code`.
- Auth and environment rules are identical to the SQL surface (`Ocp-Apim-Subscription-Key`). See `conventions/halo-connect-conventions.yml`.
