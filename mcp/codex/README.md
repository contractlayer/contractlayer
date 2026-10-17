# eContract MCP server in Codex

Connect eContract to Codex, OpenAI’s coding agent. The CLI and the IDE extension share the same configuration.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add the server and sign in with the commands below. codex mcp login opens the eContract sign-in page in your browser.
2. In the IDE extension you can instead open the settings menu → MCP servers → Add server, choose Streamable HTTP, enter https://api.econtract.online/mcp and restart the extension.

`Terminal`

```bash
codex mcp add econtract --url https://api.econtract.online/mcp
codex mcp login econtract
```

## Use an API key

For unattended runs. Create a key, store it in the ECONTRACT_API_KEY environment variable and keep it out of shared files.

1. Set the ECONTRACT_API_KEY environment variable to your API key.
2. Add the server to ~/.codex/config.toml. Codex sends the key as a Bearer token.

`~/.codex/config.toml`

```toml
[mcp_servers.econtract]
url = "https://api.econtract.online/mcp"
bearer_token_env_var = "ECONTRACT_API_KEY"
```

Create an API key in the eContract dashboard: https://econtract.online/dashboard/api-keys

_These steps follow the official Codex documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- Codex MCP documentation: https://learn.chatgpt.com/docs/extend/mcp?surface=cli
- This guide on the eContract site: https://econtract.online/mcp/codex
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
