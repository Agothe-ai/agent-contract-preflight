# Agothe Agent Contract Preflight

**Canonical MCP identity:** `ai.agothe.mcp-chatgpt/agent-contract-preflight`  
**Version:** `0.2.0`  
**Remote MCP endpoint:** `https://mcp-chatgpt.agothe.ai/mcp`  
**Transport:** Streamable HTTP  
**OAuth scope:** `agothe:muv`

This repository is the **public discovery and trust metadata surface** for Agothe Agent Contract Preflight. It is **not a second MCP implementation** and does not mirror the private runtime.

## Start here

**Product page:** https://agothe.ai/mcp-breaking-change-checker

Use Agent Contract Preflight when you want to check an MCP or agent-tool contract **before release** for schema incompatibility, breaking changes, and SemVer mistakes.

For an OAuth-capable MCP client, the canonical remote server is:

`https://mcp-chatgpt.agothe.ai/mcp`

Authorization uses the bounded `agothe:muv` scope. A good first utility call is `preflight_agent_contract`.

If you discovered the product through GitHub, this bounded attribution entrance is available before connection:

https://mcp-chatgpt.agothe.ai/discover/github

Live machine-readable trust facts:

https://mcp-chatgpt.agothe.ai/.well-known/agothe-muv-trust

## What it does

Preflight an agent/tool release before it breaks downstream consumers.

Search language:
- MCP schema validator
- MCP breaking-change checker
- JSON Schema compatibility
- SemVer release validation
- agent contract preflight

The four contract-analysis tools are deterministic static analysis over caller-supplied contract inputs. They do **not** use model inference or external fetches in the analysis path.

## Public tools

Exactly seven tools are exposed under `agothe:muv`:

- `validate_mcp_contract`
- `check_json_schema_compatibility`
- `check_semver_release`
- `preflight_agent_contract`
- `muv_get_balance`
- `muv_start_checkout`
- `muv_reconcile_checkout`

Canonical sorted-LF allowlist SHA-256:

`c45eee1dc8fca6a65723d8b714500201f09e689b2dce1a9e2b6dfd316f118398`

The public scope grants **no filesystem, shell, Docker, memory-write, read-context, or Stripe-administration capability**.

## Trust and privacy

Machine-readable live trust facts:

`https://mcp-chatgpt.agothe.ai/.well-known/agothe-muv-trust`

Health:

`https://mcp-chatgpt.agothe.ai/health`

Telemetry is designed to measure discovery → first use → repeat use → verified payment without persisting customer schema bodies, prompt/request bodies, OAuth or wallet tokens, raw wallet/payment identifiers, email, IP, or user-agent values.

## Billing

Machine Utility Vending credits.

- live checkout: **$1 USD**
- credits on verified paid reconciliation: **100**
- checkout creation is **not** payment
- revenue is recognized only from verified paid/reconciled evidence

## Source-tagged discovery entrances

These URLs exist only to attribute a bounded source label before OAuth. They reject query parameters and do not persist referrer URLs or UTM payloads.

- Official Registry: `https://mcp-chatgpt.agothe.ai/discover/official_registry`
- GitHub: `https://mcp-chatgpt.agothe.ai/discover/github`
- Glama: `https://mcp-chatgpt.agothe.ai/discover/glama`
- Smithery: `https://mcp-chatgpt.agothe.ai/discover/smithery`
- MCP.so: `https://mcp-chatgpt.agothe.ai/discover/mcp_so`
- Web: `https://mcp-chatgpt.agothe.ai/discover/web`
- Direct: `https://mcp-chatgpt.agothe.ai/discover/direct`

## Canonical metadata

The canonical MCP Registry metadata is mirrored in `server.json` for discovery consistency. The hosted runtime remains the single execution source at `https://mcp-chatgpt.agothe.ai/mcp`.
