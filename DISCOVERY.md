# Discovery Identity

All discovery surfaces must point to the same product and runtime:

- Product: Agothe Agent Contract Preflight
- Registry name: `ai.agothe.mcp-chatgpt/agent-contract-preflight`
- Version: `0.2.0`
- MCP endpoint: `https://mcp-chatgpt.agothe.ai/mcp`
- OAuth scope: `agothe:muv`
- Public tool count: `7`
- Checkout price: `$1 USD / 100 credits`
- Runtime claim: deterministic static analysis for the four contract-analysis tools
- Trust: `https://mcp-chatgpt.agothe.ai/.well-known/agothe-muv-trust`

Use the source-tagged entrance for the listing itself, then direct users/agents to the canonical MCP endpoint during connection:

- GitHub: https://mcp-chatgpt.agothe.ai/discover/github
- Glama: https://mcp-chatgpt.agothe.ai/discover/glama
- Smithery: https://mcp-chatgpt.agothe.ai/discover/smithery
- MCP.so: https://mcp-chatgpt.agothe.ai/discover/mcp_so
- Official Registry: https://mcp-chatgpt.agothe.ai/discover/official_registry

No directory may advertise extra tools, a different endpoint, or different pricing/security claims.
