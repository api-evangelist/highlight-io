# Highlight (highlight.io) (highlight-io)

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
