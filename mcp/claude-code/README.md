# eContract MCP server in Claude Code

Connect eContract to Claude Code, Anthropic’s coding agent for the terminal and IDEs.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add the server for all your projects with the command below.
2. Start Claude Code, run /mcp, select econtract and sign in to eContract in the browser.

`Terminal`

```bash
claude mcp add --transport http --scope user econtract https://api.econtract.online/mcp
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Add the server to .mcp.json in your project. Claude Code reads the key from the environment, so the file holds no secret.

`.mcp.json`

```json
{
  "mcpServers": {
    "econtract": {
      "type": "http",
      "url": "https://api.econtract.online/mcp",
      "headers": {
        "Authorization": "Bearer ${ECONTRACT_API_KEY}"
      }
    }
  }
}
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Claude Code documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Claude Code MCP documentation: https://code.claude.com/docs/en/mcp
- This guide on the eContract site: https://econtract.online/mcp/claude-code
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
