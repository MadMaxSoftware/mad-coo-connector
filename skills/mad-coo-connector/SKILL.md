---
name: mad-coo-connector
description: Route supported operations requests to the authenticated MAD COO Staging Preview remote MCP tools.
---

# MAD COO Staging Preview connector

Use the configured MAD COO Staging Preview remote MCP connection for operating
context, order review, approval-labelled acknowledgement or material proposals,
schedule proposals, readiness status, and the admin-only non-mutating
expected-plan mismatch probe when the service exposes it.

Package identity: **MAD COO Staging Preview** (connector package
`mad-coo-trusted-beta`). Visible connector version must stay current with the
licensed cloud MCP; if the installed connector lags (for example an older
`0.3.0-beta.1` or mismatched marketplace label), refresh from the reviewed
thin-connector source or the owner-approved public connector-only distribution.
Do not replace this product with a full internal plugin.

- Never ask the user for a tenant identifier; authorization resolves tenancy.
- Never claim an external write completed from a proposal result.
- Preserve `[DRAFT FOR EXPLICIT APPROVAL]` and
  `Pending manual verification.` exactly when returned.
- If a tool is unavailable or authorization fails, stop and report the failure.
- Do not invent or persist entitlement/catalog changes from the mismatch probe.

This package contains routing guidance only. Workflow policy, proprietary
skills, and tenant data remain on the licensed cloud service.
