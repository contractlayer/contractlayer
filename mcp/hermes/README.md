# eContract MCP server in Hermes Agent

Connect eContract to Hermes Agent by Nous Research.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add eContract under mcp_servers in ~/.hermes/config.yaml.
2. Run /reload-mcp or restart Hermes. On first connect Hermes prints a sign-in link and opens your browser: sign in to eContract and approve access.

`~/.hermes/config.yaml`

```yaml
mcp_servers:
  econtract:
    url: "https://api.econtract.online/mcp"
    auth: oauth
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Use this configuration instead, then run /reload-mcp. Hermes fills in environment variables in the headers when it connects.

`~/.hermes/config.yaml`

```yaml
mcp_servers:
  econtract:
    url: "https://api.econtract.online/mcp"
    headers:
      Authorization: "Bearer ${ECONTRACT_API_KEY}"
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Hermes Agent documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Hermes Agent MCP documentation: https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp
- This guide on the eContract site: https://econtract.online/mcp/hermes
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
