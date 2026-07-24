# Halo Connect (halo-connect)

Halo Connect is an Australian healthcare interoperability platform, founded in 2021 and headquartered in Brisbane, Queensland, that makes primary-care data integration simple by exposing on-premise practice management system (PMS) databases through a modern cloud API. Its Halo Link agent and Halo Cloud service let approved software integrators query systems such as Best Practice, Zedmed, and Dental4Windows using either SQL passthrough or a standards-based FHIR R4 API built toward the AU Base 4.1.0 implementation guide. Halo Connect built the first FHIR API for the Best Practice Premier medical-practice industry, runs on Microsoft Azure hosted in Australia, and gates access behind a Halo Cloud subscription.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/halo-connect/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/halo-connect/refs/heads/main/apis.yml)

## Tags

- Healthcare
- Australia
- FHIR
- HL7
- Interoperability
- EHR
- Practice Management
- Primary Care
- AU Base
- Health Data

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Halo Cloud API for Integrators

The Halo Cloud API for third-party software integrators to query on-premise PMS databases over the cloud — site pairing, SQL passthrough (immediate and async queries), FHIR R4 resource search, and registered (recurring) queries. Authenticated with an Azure API Management subscription key.

- **Human URL:** [https://docs.haloconnect.io/halo-cloud/overview/](https://docs.haloconnect.io/halo-cloud/overview/)
- **Base URL:** `https://api.haloconnect.io`

#### Properties

- [OpenAPI](openapi/halo-connect-integrator-openapi.json) — OpenAPI 3.1.1, 15 paths
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [API Reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)

### Halo Cloud API for Desktop Applications

The Halo Cloud API for desktop applications — a token endpoint plus SQL passthrough, FHIR R4 resource search, and registered-query operations under `/desktop`. Authenticated with a subscription key, a bearer JWT, and a device identifier header.

- **Human URL:** [https://docs.haloconnect.io/halo-cloud/overview/](https://docs.haloconnect.io/halo-cloud/overview/)
- **Base URL:** `https://api.haloconnect.io`

#### Properties

- [OpenAPI](openapi/halo-connect-desktop-openapi.json) — OpenAPI 3.1.1, 10 paths
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [API Reference](https://docs.haloconnect.io/api-reference/desktop-openapi.html)

### Halo Cloud FHIR API

Halo Connect's FHIR API for accessing primary-care data from on-premise PMS, based on FHIR Release 4 (R4) version 4.0.1 and built toward the AU Base 4.1.0 implementation guide. Requests are site-scoped under `https://api.haloconnect.io/integrator/sites/{haloGuid}/fhir/R4/{resourceType}` and support search, read, and the Patient `$summary` operation. A live CapabilityStatement is served at `{baseUrl}/metadata` behind subscription authentication.

- **Human URL:** [https://docs.haloconnect.io/halo-cloud/fhir-api/overview/](https://docs.haloconnect.io/halo-cloud/fhir-api/overview/)
- **Base URL:** `https://api.haloconnect.io`

#### Properties

- [OpenAPI](openapi/halo-connect-integrator-openapi.json) — FHIR R4 operations are described in the Integrator spec
- [Documentation](https://docs.haloconnect.io/halo-cloud/fhir-api/overview/)
- [Documentation](https://docs.haloconnect.io/halo-cloud/fhir-api/capabilities/)
- [API Reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)

## Common Properties

- [Website](https://haloconnect.io/)
- [Developer Portal](https://docs.haloconnect.io/)
- [Documentation](https://docs.haloconnect.io/)
- [API Reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- [Getting Started](https://docs.haloconnect.io/halo-cloud/getting-started/)
- [Status Page](https://status.haloconnect.io/)
- [Trust Center](https://haloconnect.io/trust)
- [Blog](https://haloconnect.io/blog/all)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
