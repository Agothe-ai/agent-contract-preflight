# Security and Trust Boundary

Agothe Agent Contract Preflight is intentionally exposed through a narrow public aperture.

## OAuth boundary

Scope: `agothe:muv`

That scope is isolated from owner/read/operator scopes and exposes exactly seven public MUV tools.

It does not grant filesystem, shell, Docker, memory-write, read-context, or Stripe-administration capability.

## Contract-analysis behavior

`validate_mcp_contract`, `check_json_schema_compatibility`, `check_semver_release`, and `preflight_agent_contract` are deterministic static-analysis tools over caller-supplied contract artifacts.

For these four tools:
- model inference: false
- external fetch: false

## Commerce boundary

`muv_start_checkout` creates a live Stripe Checkout Session only. It does not confirm, capture, retry, or fabricate payment.

`muv_reconcile_checkout` recognizes paid state only after verified payment evidence and mints credits only after verified wallet-bound reconciliation.

## Privacy

Public telemetry does not persist customer schema bodies, prompt/request bodies, OAuth or wallet tokens, raw wallet/payment identifiers, email, IP address, or user-agent values.

Live trust facts: https://mcp-chatgpt.agothe.ai/.well-known/agothe-muv-trust
