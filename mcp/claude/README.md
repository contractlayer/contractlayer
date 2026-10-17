# eContract MCP server in Claude

Add eContract as a custom connector in Claude on the web, Claude Desktop or Cowork. Custom connectors are available on the Free, Pro, Max, Team and Enterprise plans.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Open Customize → Connectors, click “+ Add” and choose “Add custom connector”. On Team and Enterprise plans an Owner first adds it under Organization settings → Connectors (Add → Custom → Web); members then click “Connect”.
2. Name it eContract, paste the server URL https://api.econtract.online/mcp and click Continue.
3. Keep OAuth as the authentication method and click Add.
4. Sign in to eContract in the window that opens, choose the workspace and approve the requested permissions.

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Follow steps 1 and 2 above, then choose to authenticate with request headers instead of OAuth.
2. Add the Authorization header with the value Bearer followed by your API key.

`Request header`

```bash
Authorization: Bearer cl_live_…
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Claude documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Claude MCP documentation: https://support.claude.com/en/articles/11175166-getting-started-with-custom-connectors-using-remote-mcp
- This guide on the eContract site: https://econtract.online/mcp/claude
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
