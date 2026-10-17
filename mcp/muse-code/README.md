# eContract MCP server in Muse Code

Connect eContract to Muse Code, Meta’s terminal coding agent.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add eContract to the mcp_servers block of ~/.config/muse/settings.json.
2. Run muse mcp login econtract and sign in to eContract in the browser. Muse Code keeps and renews the token for you.

`~/.config/muse/settings.json`

```json
{
  "schema_version": 1,
  "mcp_servers": {
    "econtract": {
      "transport": "streamable_http",
      "url": "https://api.econtract.online/mcp"
    }
  }
}
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Use this configuration instead. Muse Code fills in environment variables in the headers.

`~/.config/muse/settings.json`

```json
{
  "schema_version": 1,
  "mcp_servers": {
    "econtract": {
      "transport": "streamable_http",
      "url": "https://api.econtract.online/mcp",
      "headers": {
        "Authorization": "Bearer ${ECONTRACT_API_KEY}"
      }
    }
  }
}
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Muse Code documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Muse Code MCP documentation: https://dev.meta.ai/docs/muse-code/extending
- This guide on the eContract site: https://econtract.online/mcp/muse-code
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
