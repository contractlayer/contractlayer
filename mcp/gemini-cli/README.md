# eContract MCP server in Gemini CLI

Connect eContract to Gemini CLI, Google’s open-source terminal agent.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add the server with the command below.
2. Start Gemini CLI and run /mcp auth econtract to sign in to eContract in the browser.

`Terminal`

```bash
gemini mcp add --transport http econtract https://api.econtract.online/mcp
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Add the server with the key in the Authorization header.

`Terminal`

```bash
gemini mcp add --transport http --header "Authorization: Bearer $ECONTRACT_API_KEY" econtract https://api.econtract.online/mcp
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Gemini CLI documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Gemini CLI MCP documentation: https://geminicli.com/docs/tools/mcp-server/
- This guide on the eContract site: https://econtract.online/mcp/gemini-cli
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
