# eContract MCP server in VS Code (GitHub Copilot)

Connect eContract to GitHub Copilot’s agent mode in Visual Studio Code.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Open the Command Palette (Ctrl+Shift+P, or Shift+Cmd+P on macOS) and run MCP: Add Server.
2. Choose HTTP, paste https://api.econtract.online/mcp and name the server econtract.
3. When VS Code asks you to sign in, approve access on the eContract page that opens.

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Add the configuration below to .mcp.json at the root of your workspace.
2. When the server starts, VS Code asks for the API key once and stores it securely.

`.mcp.json`

```json
{
  "mcpServers": {
    "econtract": {
      "type": "http",
      "url": "https://api.econtract.online/mcp",
      "headers": {
        "Authorization": "Bearer ${input:econtract-api-key}"
      }
    }
  },
  "inputs": [
    {
      "id": "econtract-api-key",
      "type": "promptString",
      "description": "eContract API key",
      "password": true
    }
  ]
}
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official VS Code (GitHub Copilot) documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- VS Code (GitHub Copilot) MCP documentation: https://code.visualstudio.com/docs/copilot/customization/mcp-servers
- This guide on the eContract site: https://econtract.online/mcp/vscode
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
