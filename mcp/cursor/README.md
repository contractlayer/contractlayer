# eContract MCP server in Cursor

Connect eContract to Cursor so its agent can prepare and send contracts from the editor.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add eContract to ~/.cursor/mcp.json (all projects) or .cursor/mcp.json (one project).
2. Reload Cursor and, when it asks you to authenticate the server, sign in to eContract in the browser.

`~/.cursor/mcp.json`

```json
{
  "mcpServers": {
    "econtract": {
      "url": "https://api.econtract.online/mcp"
    }
  }
}
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Use this configuration instead. Cursor reads the key from the environment variable.

`~/.cursor/mcp.json`

```json
{
  "mcpServers": {
    "econtract": {
      "url": "https://api.econtract.online/mcp",
      "headers": {
        "Authorization": "Bearer ${env:ECONTRACT_API_KEY}"
      }
    }
  }
}
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Cursor documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Cursor MCP documentation: https://cursor.com/docs/context/mcp
- This guide on the eContract site: https://econtract.online/mcp/cursor
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
