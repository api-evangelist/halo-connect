# Halo Connect (halo-connect)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
