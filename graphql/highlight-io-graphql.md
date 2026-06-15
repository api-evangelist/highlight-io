# Highlight (highlight.io) GraphQL API

GraphQL-over-HTTP session replay ingestion endpoint at `https://pub.highlight.io` used by the `highlight.run` browser SDK to upload rrweb DOM snapshots, console/network recording, custom events, identify payloads, and error reports. Public, project-id authenticated, no user secrets required.

## Highlight Session Ingestion API

**Documentation:** https://www.highlight.io/docs/general/product-features/session-replay

**References:**

- Documentation: https://www.highlight.io/docs/general/product-features/session-replay

## Highlight Private GraphQL API

Internal GraphQL API that powers the Highlight dashboard at `https://pri.highlight.io`. Used to list, search, and manage workspaces, projects, sessions, errors, logs, traces, dashboards, alerts, and integrations. Authenticated via dashboard session cookie or workspace admin API token; the schema is open-source under `backend/private-graph/graph` but is not a stable public contract.

**Documentation:** https://github.com/highlight/highlight/tree/main/backend/private-graph

**References:**

- Documentation: https://github.com/highlight/highlight/tree/main/backend/private-graph
- Documentation: https://www.highlight.io/docs/general/product-features/general-features/api
