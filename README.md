# Highlight (highlight-io)

Highlight (highlight.io) is the open-source, full-stack monitoring platform — session replay, error monitoring, logging, distributed tracing, and metrics in a single tool. Built on OpenTelemetry, rrweb, and ClickHouse, Highlight correlates server-side spans and logs back to the originating browser session so engineers can move from a customer report to the exact line of code in one click. Available as a hosted SaaS on three commercial tiers (Free / Pay-as-you-go / Business / Enterprise) and as a fully open-source self-hosted deployment (Dev / Hobby / Enterprise) under Apache 2.0.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/highlight-io/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Observability, Session Replay, Error Monitoring, APM, Logging, Tracing, OpenTelemetry, Open Source, Frontend Monitoring, Full Stack Monitoring

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## At a Glance

| Surface | Endpoint | Auth | Format |
|---|---|---|---|
| Session ingestion (rrweb) | `https://pub.highlight.io/` | Public project verbose ID | GraphQL over HTTP |
| OTLP traces | `https://otel.highlight.io/v1/traces` | Project ID resource attribute | OTLP HTTP/JSON or Protobuf |
| OTLP logs | `https://otel.highlight.io/v1/logs` | Project ID resource attribute | OTLP HTTP/JSON or Protobuf |
| OTLP metrics (beta) | `https://otel.highlight.io/v1/metrics` | Project ID resource attribute | OTLP HTTP/JSON or Protobuf |
| Dashboard backend | `https://pri.highlight.io/` | Workspace API token | GraphQL over HTTP |
| Outbound webhooks | Customer-supplied URL | Customer-supplied secret | JSON POST |

## APIs

### Highlight OTLP Traces API
Native OpenTelemetry Protocol HTTP/JSON ingestion for distributed traces. Spans carry `highlight.project_id` for routing and optional `highlight.session_id` / `highlight.trace_id` for correlation with the browser session.

**Human URL:** [https://www.highlight.io/docs/general/product-features/tracing](https://www.highlight.io/docs/general/product-features/tracing)

- [Documentation](https://www.highlight.io/docs/general/product-features/tracing)
- [OpenAPI](openapi/highlight-otlp-traces-api-openapi.yml)
- [JSON Schema — Trace](json-schema/highlight-trace-schema.json)
- [Naftiko Capability — OTLP Traces](capabilities/otlp-traces.yaml)

### Highlight OTLP Logs API
Native OpenTelemetry Protocol HTTP/JSON ingestion for structured logs. Stored in ClickHouse for sub-second full-text search and pattern detection.

**Human URL:** [https://www.highlight.io/docs/general/product-features/logging](https://www.highlight.io/docs/general/product-features/logging)

- [Documentation](https://www.highlight.io/docs/general/product-features/logging)
- [OpenAPI](openapi/highlight-otlp-logs-api-openapi.yml)
- [JSON Schema — Log](json-schema/highlight-log-schema.json)
- [Naftiko Capability — OTLP Logs](capabilities/otlp-logs.yaml)

### Highlight OTLP Metrics API (beta)
Native OpenTelemetry Protocol HTTP/JSON ingestion for metrics — gauges, sums, histograms, and exponential histograms — that drive dashboards, monitors, and the metrics SQL editor.

**Human URL:** [https://www.highlight.io/docs/general/product-features/metrics](https://www.highlight.io/docs/general/product-features/metrics)

- [Documentation](https://www.highlight.io/docs/general/product-features/metrics)
- [OpenAPI](openapi/highlight-otlp-metrics-api-openapi.yml)
- [Naftiko Capability — OTLP Metrics](capabilities/otlp-metrics.yaml)

### Highlight Session Ingestion API
GraphQL-over-HTTP endpoint at `pub.highlight.io` used by the `highlight.run` browser SDK to upload rrweb DOM snapshots, console/network recording, identify payloads, custom events, and frontend errors.

**Human URL:** [https://www.highlight.io/docs/general/product-features/session-replay](https://www.highlight.io/docs/general/product-features/session-replay)

- [Documentation](https://www.highlight.io/docs/general/product-features/session-replay)
- [OpenAPI](openapi/highlight-session-ingestion-api-openapi.yml)
- [JSON Schema — Session](json-schema/highlight-session-schema.json)
- [Naftiko Capability — Session Ingestion](capabilities/session-ingestion.yaml)

### Highlight Private GraphQL API
Internal GraphQL surface at `pri.highlight.io` that powers the dashboard — workspaces, projects, sessions, errors, logs, traces, dashboards, alerts, integrations. Open-source under `backend/private-graph/graph` but not a stable public contract.

**Human URL:** [https://github.com/highlight/highlight/tree/main/backend/private-graph](https://github.com/highlight/highlight/tree/main/backend/private-graph)

- [Source](https://github.com/highlight/highlight/tree/main/backend/private-graph)
- [Naftiko Capability — Private GraphQL](capabilities/private-graphql.yaml)

### Highlight Webhooks API
Outbound JSON webhooks delivered when alerts fire (Error, Session, User, Log, Trace, Metric monitor). Carries alert metadata, project routing, and action URLs to resolve, ignore, or snooze the source event.

**Human URL:** [https://www.highlight.io/docs/general/product-features/general-features/webhooks](https://www.highlight.io/docs/general/product-features/general-features/webhooks)

- [Documentation](https://www.highlight.io/docs/general/product-features/general-features/webhooks)
- [OpenAPI](openapi/highlight-webhooks-api-openapi.yml)
- [Naftiko Capability — Webhooks Receiver](capabilities/webhooks-receiver.yaml)

### Highlight Self-Hosted Deployment
Self-hosted deployment of the open-source Highlight stack. Three tiers — Dev (docker-compose), Hobby (single-host Docker), Enterprise (Kubernetes). All ingestion endpoints (`pub`, `pri`, `otel`) are reproduced in-cluster.

**Human URL:** [https://www.highlight.io/docs/general/company/open-source/self-host-hobby](https://www.highlight.io/docs/general/company/open-source/self-host-hobby)

- [Self-Host (Hobby)](https://www.highlight.io/docs/general/company/open-source/self-host-hobby)
- [Self-Host (Enterprise)](https://www.highlight.io/docs/general/company/open-source/self-host-enterprise)
- [Docker source](https://github.com/highlight/highlight/tree/main/docker)

## SDKs

**Browser:** `highlight.run`, `@highlight-run/react`, `@highlight-run/next`, `@highlight-run/remix`, `@highlight-run/sveltekit`, plus framework-specific bundles for Vue, Angular, Gatsby, Electron, React Native (beta).

**Server (Node):** `@highlight-run/node`, `@highlight-run/next`, `@highlight-run/nest`, `@highlight-run/cloudflare` — submodules cover Express, NestJS, Apollo, AWS Lambda, Cloudflare Workers, Firebase, Hono, tRPC, Winston, Pino.

**Other languages:** Go, Python, Ruby, Rust, Elixir, Java, PHP, C#/.NET — all published from the [highlight monorepo](https://github.com/highlight/highlight/tree/main/sdk).

## Plans, Rate Limits, FinOps

- [Plans & Pricing (API Commons 0.1)](plans/highlight-io-plans-pricing.yml)
- [Rate Limits (API Commons 0.1)](rate-limits/highlight-io-rate-limits.yml)
- [FinOps (FOCUS 1.3)](finops/highlight-io-finops.yml)

## Semantics, Schemas, and Rules

- [JSON-LD Context](json-ld/highlight-io-context.jsonld)
- [Vocabulary](vocabulary/highlight-io-vocabulary.yml)
- [Spectral Ruleset](rules/highlight-io-rules.yml)

## Open Source

- **Repository:** [github.com/highlight/highlight](https://github.com/highlight/highlight) — 9,000+ stars
- **License:** Apache 2.0 (with separate license for the `highlight.io/` site directory and the `enterprise/` directory)
- **Languages:** TypeScript (frontend, SDKs), Go (backend, collectors)
- **Storage:** ClickHouse (sessions, errors, logs, traces, metrics), Postgres (metadata), Kafka (ingestion buffer)

## Maintainer

- Kin Lane — [apievangelist.com](https://apievangelist.com)
