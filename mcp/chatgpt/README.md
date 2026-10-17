# eContract MCP server in ChatGPT

Add eContract to ChatGPT as an MCP app in developer mode. At the time of writing, full MCP support with write actions is in beta for ChatGPT Business, Enterprise and Edu, and a workspace admin may need to allow it.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Open Settings → Apps → Advanced settings and turn on Developer mode.
2. Click Create app, name it eContract and enter the MCP server URL https://api.econtract.online/mcp.
3. Choose OAuth as the authentication method and save.
4. Sign in to eContract when ChatGPT opens the authorization page, then approve the requested permissions.

_These steps follow the official ChatGPT documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- ChatGPT MCP documentation: https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt
- This guide on the eContract site: https://econtract.online/mcp/chatgpt
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
