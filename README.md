# Highlight (highlight.io) (highlight-io)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/highlight-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/highlight-io/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Observability
- Session Replay
- Error Monitoring
- APM
- Logging
- Tracing
- OpenTelemetry
- Open Source
- Frontend Monitoring
- Full Stack Monitoring

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Highlight OTLP Traces API

Native OpenTelemetry Protocol (OTLP) HTTP/JSON ingestion endpoint for distributed traces. Accepts standard OTLP `ResourceSpans` payloads at `https://otel.highlight.io/v1/traces`. Spans carry the `highlight.project_id` resource attribute and optional `highlight.session_id` / `highlight.trace_id` so server-side spans correlate with frontend session replay.

- **Human URL:** [https://www.highlight.io/docs/general/product-features/tracing](https://www.highlight.io/docs/general/product-features/tracing)

#### Tags

- Observability
- OpenTelemetry
- Traces
- Tracing
- Distributed Tracing

#### Properties

- [Documentation](https://www.highlight.io/docs/general/product-features/tracing)
- [OpenAPI](openapi/highlight-otlp-traces-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/highlight-otlp-traces-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-traces-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/highlight-trace-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Highlight OTLP Logs API

Native OpenTelemetry Protocol (OTLP) HTTP/JSON ingestion endpoint for structured logs at `https://otel.highlight.io/v1/logs`. Supports severity levels, trace/span correlation, and arbitrary attributes. Highlight stores logs in ClickHouse for sub-second full-text search and pattern detection.

- **Human URL:** [https://www.highlight.io/docs/general/product-features/logging](https://www.highlight.io/docs/general/product-features/logging)

#### Tags

- Observability
- OpenTelemetry
- Logs
- Logging

#### Properties

- [Documentation](https://www.highlight.io/docs/general/product-features/logging)
- [OpenAPI](openapi/highlight-otlp-logs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/highlight-otlp-logs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-logs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/highlight-log-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Highlight OTLP Metrics API

Beta OpenTelemetry Protocol (OTLP) HTTP/JSON ingestion endpoint for metrics at `https://otel.highlight.io/v1/metrics`. Accepts gauges, sums, histograms, and exponential histograms and drives Highlight dashboards, alerts, and the metrics SQL editor.

- **Human URL:** [https://www.highlight.io/docs/general/product-features/metrics](https://www.highlight.io/docs/general/product-features/metrics)

#### Tags

- Observability
- OpenTelemetry
- Metrics
- Beta

#### Properties

- [Documentation](https://www.highlight.io/docs/general/product-features/metrics)
- [OpenAPI](openapi/highlight-otlp-metrics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/highlight-otlp-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Highlight Session Ingestion API

GraphQL-over-HTTP session replay ingestion endpoint at `https://pub.highlight.io` used by the `highlight.run` browser SDK to upload rrweb DOM snapshots, console/network recording, custom events, identify payloads, and error reports. Public, project-id authenticated, no user secrets required.

- **Human URL:** [https://www.highlight.io/docs/general/product-features/session-replay](https://www.highlight.io/docs/general/product-features/session-replay)

#### Tags

- Observability
- Session Replay
- Ingestion
- GraphQL

#### Properties

- [Documentation](https://www.highlight.io/docs/general/product-features/session-replay)
- [OpenAPI](openapi/highlight-session-ingestion-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/highlight-session-ingestion-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-session-ingestion-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/highlight-session-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Highlight Private GraphQL API

Internal GraphQL API that powers the Highlight dashboard at `https://pri.highlight.io`. Used to list, search, and manage workspaces, projects, sessions, errors, logs, traces, dashboards, alerts, and integrations. Authenticated via dashboard session cookie or workspace admin API token; the schema is open-source under `backend/private-graph/graph` but is not a stable public contract.

- **Human URL:** [https://github.com/highlight/highlight/tree/main/backend/private-graph](https://github.com/highlight/highlight/tree/main/backend/private-graph)

#### Tags

- Observability
- GraphQL
- Management
- Internal

#### Properties

- [Documentation](https://github.com/highlight/highlight/tree/main/backend/private-graph)
- [Documentation](https://www.highlight.io/docs/general/product-features/general-features/api)
- [Postman Collection](collections/highlight-otlp-logs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-logs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-traces-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-traces-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-session-ingestion-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-session-ingestion-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Highlight Webhooks API

Outbound webhooks delivered when Highlight alerts fire. POST JSON payload to a customer-supplied URL with alert metadata (name, type, count), error/session/log/metric context, project routing, and action URLs to resolve, ignore, or snooze. Supports Error, Session, User, Log, Trace, and Metric monitor alerts.

- **Human URL:** [https://www.highlight.io/docs/general/product-features/general-features/webhooks](https://www.highlight.io/docs/general/product-features/general-features/webhooks)

#### Tags

- Observability
- Webhooks
- Alerts
- Notifications

#### Properties

- [Documentation](https://www.highlight.io/docs/general/product-features/general-features/webhooks)
- [Async Events](openapi/highlight-webhooks-api-openapi.yml)
- [Postman Collection](collections/highlight-otlp-logs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-logs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-traces-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-traces-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-session-ingestion-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-session-ingestion-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Highlight Self-Hosted Deployment

Self-hosted deployment of the open-source Highlight stack. Three tiers — Dev (single-host docker-compose), Hobby (single-host Docker for low-volume production), and Enterprise (Kubernetes with horizontal scaling, ClickHouse cluster, and managed retention). All ingestion endpoints (OTLP traces, logs, metrics; pub.highlight.io session ingestion; pri.highlight.io GraphQL) are reproduced in-cluster.

- **Human URL:** [https://www.highlight.io/docs/general/company/open-source/self-host-hobby](https://www.highlight.io/docs/general/company/open-source/self-host-hobby)

#### Tags

- Observability
- Self-Hosted
- Open Source
- Docker
- Kubernetes

#### Properties

- [Documentation](https://www.highlight.io/docs/general/company/open-source/self-host-hobby)
- [Documentation](https://www.highlight.io/docs/general/company/open-source/self-host-enterprise)
- [Source Code](https://github.com/highlight/highlight/tree/main/docker)
- [Postman Collection](collections/highlight-otlp-logs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-logs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-otlp-traces-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-otlp-traces-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-session-ingestion-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-session-ingestion-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/highlight-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/highlight-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://www.highlight.io)
- [Documentation](https://www.highlight.io/docs)
- [Getting Started](https://www.highlight.io/docs/general/welcome)
- [Sign Up](https://app.highlight.io/sign_up)
- [Portal](https://app.highlight.io)
- [Pricing](https://www.highlight.io/pricing)
- [Case Studies](https://www.highlight.io/customers)
- [Blog](https://www.highlight.io/blog)
- [Changelog](https://www.highlight.io/changelog)
- [Status Page](https://status.highlight.io)
- [Forum](https://www.highlight.io/community)
- [Forum](https://discord.gg/yxaXEAqgwN)
- [Source Code](https://github.com/highlight/highlight)
- [GitHub Organization](https://github.com/highlight)
- [Documentation](https://www.highlight.io/docs/general/company/open-source/hosted-vs-self-hosted)
- [Documentation](https://www.highlight.io/docs/general/company/open-source/self-host-hobby)
- [Documentation](https://www.highlight.io/docs/general/company/open-source/self-host-enterprise)
- [Compliance](https://www.highlight.io/docs/general/company/security-and-privacy/compliance)
- [Security](https://www.highlight.io/docs/general/company/security-and-privacy/security)
- [Terms of Service](https://www.highlight.io/terms)
- [Privacy Policy](https://www.highlight.io/privacy)
- [Roadmap](https://www.highlight.io/docs/general/company/general/roadmap)
- [Documentation](https://www.highlight.io/docs/general/company/open-source/contributing)
- [SDK](https://www.highlight.io/docs/sdk/highlightrun)
- [SDK](https://www.npmjs.com/package/highlight.run)
- [SDK](https://www.npmjs.com/package/@highlight-run/node)
- [SDK](https://www.npmjs.com/package/@highlight-run/next)
- [SDK](https://www.npmjs.com/package/@highlight-run/nest)
- [SDK](https://www.npmjs.com/package/@highlight-run/react)
- [SDK](https://www.npmjs.com/package/@highlight-run/remix)
- [SDK](https://www.npmjs.com/package/@highlight-run/sveltekit)
- [SDK](https://www.npmjs.com/package/@highlight-run/cloudflare)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-go)
- [SDK](https://pypi.org/project/highlight-io/)
- [SDK](https://rubygems.org/gems/highlight_io)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-rust)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-elixir)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-java)
- [SDK](https://github.com/highlight/highlight-php)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-dotnet)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-react-native)
- [SDK](https://github.com/highlight/highlight/tree/main/sdk/highlight-electron)
- [OpenAPI](openapi/highlight-otlp-traces-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/highlight-otlp-logs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/highlight-otlp-metrics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/highlight-session-ingestion-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/highlight-webhooks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](plans/highlight-io-plans-pricing.yml)
- [Rate Limits](rate-limits/highlight-io-rate-limits.yml)
- [Fin Ops](finops/highlight-io-finops.yml)
- [JSON-LD](json-ld/highlight-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/highlight-io-vocabulary.yml)
- [Spectral Rules](rules/highlight-io-rules.yml)
- [LinkedIn](https://www.linkedin.com/company/highlightio)
- [Twitter](https://twitter.com/highlightio)
- [YouTube](https://www.youtube.com/@highlightio)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
