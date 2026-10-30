# Highlight (highlight.io)

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

Highlight (highlight.io) is the open-source, full-stack monitoring platform — session replay, error monitoring, logging, distributed tracing, and metrics in a single tool. Built on OpenTelemetry, rrweb, and ClickHouse, Highlight correlates server-side spans and logs back to the originating browser session so engineers can move from a customer report to the exact line of code in one click. Available as a hosted SaaS on three commercial tiers (Free / Pay-as-you-go / Business / Enterprise) and as a fully open-source self-hosted deployment (Dev / Hobby / Enterprise) under Apache 2.0.

**Areas:** Observability · Session Replay · Error Monitoring · APM · Logging · Tracing · OpenTelemetry · Open Source · Frontend Monitoring · Full Stack Monitoring

## Highlight (highlight.io) on APIs.io

Everything profiled for Highlight (highlight.io) is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/highlight-io/](https://apis.io/providers/highlight-io/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Highlight Private GraphQL API](https://apis.io/apis/highlight-io/highlight-private-graphql-api/) — Internal GraphQL API that powers the Highlight dashboard at `https://pri.highlight.io`. Used to list, search, and manage workspaces, projects, sessions,…
- [Highlight Webhooks API](https://apis.io/apis/highlight-io/highlight-webhooks-api/) — Outbound webhooks delivered when Highlight alerts fire. POST JSON payload to a customer-supplied URL with alert metadata (name, type, count),…
- [Highlight Self-Hosted Deployment](https://apis.io/apis/highlight-io/highlight-self-hosted-api/) — Self-hosted deployment of the open-source Highlight stack. Three tiers — Dev (single-host docker-compose), Hobby (single-host Docker for low-volume…
- [Highlight (highlight.io) Logs API](https://apis.io/apis/highlight-io/highlight-io-logs-api/) — OpenTelemetry log ingestion
- [Highlight (highlight.io) Metrics API](https://apis.io/apis/highlight-io/highlight-io-metrics-api/) — OpenTelemetry metric ingestion (beta)
- [Highlight (highlight.io) Sessions API](https://apis.io/apis/highlight-io/highlight-io-sessions-api/) — Browser session ingestion mutations
- [Highlight (highlight.io) Traces API](https://apis.io/apis/highlight-io/highlight-io-traces-api/) — OpenTelemetry trace ingestion

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (10)

Multi-step workflows that chain operations into a business task.

- [Highlight Backend Error Report](https://apis.io/arazzos/highlight-io/highlight-io-backend-error-report-workflow/)
- [Highlight Backend Session Payload](https://apis.io/arazzos/highlight-io/highlight-io-backend-session-payload-workflow/)
- [Highlight Browser Session Lifecycle](https://apis.io/arazzos/highlight-io/highlight-io-browser-session-lifecycle-workflow/)
- [Highlight Correlated Backend Telemetry Export](https://apis.io/arazzos/highlight-io/highlight-io-correlated-backend-telemetry-export-workflow/)
- [Highlight Frontend Error Capture](https://apis.io/arazzos/highlight-io/highlight-io-frontend-error-capture-workflow/)
- [Highlight Fullstack Error Correlation](https://apis.io/arazzos/highlight-io/highlight-io-fullstack-error-correlation-workflow/)
- [Highlight Fullstack Session Correlation](https://apis.io/arazzos/highlight-io/highlight-io-fullstack-session-correlation-workflow/)
- [Highlight Logs and Metrics Batch](https://apis.io/arazzos/highlight-io/highlight-io-logs-and-metrics-batch-workflow/)
- [Highlight Session Feedback Capture](https://apis.io/arazzos/highlight-io/highlight-io-session-feedback-capture-workflow/)
- [Highlight Session Track Event](https://apis.io/arazzos/highlight-io/highlight-io-session-track-event-workflow/)

#### GraphQL (1)

GraphQL schemas.

- [Highlight (highlight.io) GraphQL API](https://apis.io/graphqls/highlight-io/highlight-io-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Highlight Io Agentic Access](https://apis.io/agentic-access/highlight-io/highlight-io-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Highlight Log Record (OTLP)](https://apis.io/schemas/highlight-io/highlight-log/)
- [Highlight Session](https://apis.io/schemas/highlight-io/highlight-session/)
- [Highlight Trace (OTLP)](https://apis.io/schemas/highlight-io/highlight-trace/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Highlight Io Context](https://apis.io/jsonld/highlight-io/highlight-io-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Highlight Io Vocabulary](https://apis.io/vocabularies/highlight-io/highlight-io-vocabulary/)

#### Collections (14)

Postman and Open Collection request collections.

- [Highlight OTLP Logs API](https://apis.io/collections/highlight-io/open-highlight-io-logs-api/)
- [Highlight OTLP Logs Metrics API](https://apis.io/collections/highlight-io/open-highlight-io-metrics-api/)
- [Highlight OTLP Logs Sessions API](https://apis.io/collections/highlight-io/open-highlight-io-sessions-api/)
- [Highlight OTLP Logs Traces API](https://apis.io/collections/highlight-io/open-highlight-io-traces-api/)
- [Highlight OTLP Logs Webhooks API](https://apis.io/collections/highlight-io/open-highlight-io-webhooks-api/)
- [Highlight OTLP Logs API](https://apis.io/collections/highlight-io/open-highlight-otlp-logs-api/)
- [Highlight OTLP Metrics API](https://apis.io/collections/highlight-io/open-highlight-otlp-metrics-api/)
- [Highlight OTLP Traces API](https://apis.io/collections/highlight-io/open-highlight-otlp-traces-api/)
- [Highlight Session Ingestion API](https://apis.io/collections/highlight-io/open-highlight-session-ingestion-api/)
- [Highlight Webhooks API](https://apis.io/collections/highlight-io/open-highlight-webhooks-api/)
- [Highlight OTLP Logs API](https://apis.io/collections/highlight-io/postman-highlight-otlp-logs-api/)
- [Highlight OTLP Metrics API](https://apis.io/collections/highlight-io/postman-highlight-otlp-metrics-api/)
- [Highlight OTLP Traces API](https://apis.io/collections/highlight-io/postman-highlight-otlp-traces-api/)
- [Highlight Session Ingestion API](https://apis.io/collections/highlight-io/postman-highlight-session-ingestion-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Highlight (highlight.io) — jsonschema rules](https://apis.io/rules/highlight-io/highlight-io-jsonschema-spectral-rules/)
- [Highlight (highlight.io) API Rules](https://apis.io/rules/highlight-io/highlight-io-rules/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Highlight Io Domain Security](https://apis.io/security/highlight-io/highlight-io-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Highlight Io Plans Pricing](https://apis.io/plans/highlight-io/highlight-io-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Highlight Io Rate Limits](https://apis.io/rate-limits/highlight-io/highlight-io-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Highlight Io Finops](https://apis.io/finops/highlight-io/highlight-io-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://highlight.io)
- [Documentation](https://www.highlight.io/docs)
- [Getting started](https://www.highlight.io/docs/general/welcome)
- [Pricing](https://www.highlight.io/pricing)
- [Changelog](https://www.highlight.io/changelog)
- [Blog](https://www.highlight.io/blog)
- [Security](https://www.highlight.io/docs/general/company/security-and-privacy/security)
- [Compliance](https://www.highlight.io/docs/general/company/security-and-privacy/compliance)
- [Terms of service](https://www.highlight.io/terms)
- [Privacy policy](https://www.highlight.io/privacy)
- [GitHub](https://github.com/highlight)
- [Status](https://status.highlight.io)

## API Evangelist rating

**Kin Score 56.9** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 56.2 |
| Contract governance | 27.3 |
| Operational transparency | 60.5 |
| Developer ergonomics | 56.0 |
| Access clarity | 68.4 |

**Agent readiness 21.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 23.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/highlight-io/](https://apis.io/providers/highlight-io/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Highlight (highlight.io): the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/highlight-io/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
