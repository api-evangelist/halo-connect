# Halo Connect

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

Halo Connect is an Australian healthcare interoperability platform, founded in 2021 and headquartered in Brisbane, Queensland, that makes primary-care data integration simple by exposing on-premise practice management system (PMS) databases through a modern cloud API. Its Halo Link agent and Halo Cloud service let approved software integrators query systems such as Best Practice, Zedmed, and Dental4Windows using either SQL passthrough or a standards-based FHIR R4 (4.0.1) API built toward the AU Base 4.1.0 implementation guide, without maintaining a separate database agent per integration. Halo Connect built the first FHIR API for the Best Practice Premier medical-practice industry. The platform runs on Microsoft Azure hosted in Australia, and access is gated behind a Halo Cloud subscription using Azure API Management subscription keys and, for desktop applications, bearer JWT tokens issued from a token endpoint; there is no self-serve public API.

**Areas:** Healthcare · Australia · FHIR · HL7 · Interoperability · Electronic Health Records · Practice Management · Primary Care · AU Base · Health Data

## Halo Connect on APIs.io

Everything profiled for Halo Connect is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/halo-connect/](https://apis.io/providers/halo-connect/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Halo Connect FHIR API](https://apis.io/apis/halo-connect/halo-connect-fhir-api/) — Query practice data using FHIR resources.
- [Halo Connect Registered Queries API](https://apis.io/apis/halo-connect/halo-connect-registered-queries-api/) — The Registered Queries API from Halo Connect — 6 operation(s) for registered queries.
- [Halo Connect Sites API](https://apis.io/apis/halo-connect/halo-connect-sites-api/) — Endpoints for practice onboarding and site metadata.
- [Halo Connect SQL Passthrough API](https://apis.io/apis/halo-connect/halo-connect-sql-passthrough-api/) — Send SQL queries to practices as immediate, async or registered queries. **Immediate queries** are small, time-sensitive queries that return a result in…
- [Halo Connect Tokens API](https://apis.io/apis/halo-connect/halo-connect-tokens-api/) — Obtain authorization tokens for desktop applications to authenticate API requests.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Halo Connect Webhooks](https://apis.io/asyncapis/halo-connect/halo-connect-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/halo-connect/querycompleted/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [halo-connect](https://apis.io/servers/halo-connect/halo-connect/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Halo Connect Agentic Access](https://apis.io/agentic-access/halo-connect/halo-connect-agentic-access/)

#### Collections (2)

Postman and Open Collection request collections.

- [Halo Cloud API for Desktop Applications](https://apis.io/collections/halo-connect/open-halo-connect-desktop/)
- [Halo Cloud API for Integrators](https://apis.io/collections/halo-connect/open-halo-connect-integrator/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Halo Connect Desktop Overlay](https://apis.io/overlays/halo-connect/halo-connect-desktop-overlay/)
- [Halo Connect Integrator Overlay](https://apis.io/overlays/halo-connect/halo-connect-integrator-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Halo Connect Authentication](https://apis.io/security/halo-connect/halo-connect-authentication/)
- [Halo Connect Domain Security](https://apis.io/security/halo-connect/halo-connect-domain-security/)
- [Halo Connect Trust Center](https://apis.io/security/halo-connect/halo-connect-trust-center/)
- [Halo Connect Vulnerability Disclosure](https://apis.io/security/halo-connect/halo-connect-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://haloconnect.io/)
- [Documentation](https://docs.haloconnect.io/)
- [Getting started](https://docs.haloconnect.io/halo-cloud/getting-started/)
- [API reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- [Support](https://haloconnect.io/contact-us)
- [Blog](https://haloconnect.io/blog)
- [Security](https://docs.haloconnect.io/security/)
- [Compliance](https://haloconnect.io/trust)
- [Trust centre](https://haloconnect.io/trust)
- [Terms of service](https://haloconnect.io/terms-and-conditions)
- [Privacy policy](https://haloconnect.io/privacy-policy)
- [Status](https://status.haloconnect.io/)

## API Evangelist rating

**Kin Score 53.8** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 59.8 |
| Contract governance | 18.2 |
| Operational transparency | 50.0 |
| Developer ergonomics | 66.1 |
| Access clarity | 36.8 |

**Agent readiness 28.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 32.0** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/halo-connect/](https://apis.io/providers/halo-connect/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Halo Connect: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/halo-connect/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
