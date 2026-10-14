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
`mad-coo-trusted-beta`, version `0.3.2-beta.1`). Install this exact package only
from the public `MadMaxSoftware/mad-coo-connector` marketplace. Max and every
limited-beta tester use this same package and the same staging MCP endpoint;
there is no owner-only or stale-plugin compatibility path.

- Never ask the user for a tenant identifier; the signed-in account resolves
  tenancy. Do not embed or infer tenant-specific identity in this connector.
- Never claim an external write completed from a proposal result.
- Preserve `[DRAFT FOR EXPLICIT APPROVAL]` and
  `Pending manual verification.` exactly when returned.
- If a tool is unavailable or authorization fails, stop and report the failure.
- Do not invent or persist entitlement/catalog changes from the mismatch probe.

This package contains routing guidance only. Workflow policy, proprietary
skills, and tenant data remain on the licensed cloud service.
