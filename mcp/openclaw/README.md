# eContract MCP server in OpenClaw

Connect eContract to OpenClaw so your personal assistant can send contracts and follow their signing.

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP)

## Sign in with OAuth

Recommended for personal use: you sign in once and the client keeps the connection alive.

1. Add the server with openclaw mcp add (first command below).
2. Run openclaw mcp login econtract and approve access in the browser. An administrator can also click Sign in for the server in the Control UI settings.
3. Check the connection with openclaw mcp doctor econtract --probe.

`Terminal`

```bash
openclaw mcp add econtract --url https://api.econtract.online/mcp --transport streamable-http
openclaw mcp login econtract
openclaw mcp doctor econtract --probe
```

_These steps follow the official OpenClaw documentation as of 2026-10. If the menus have changed since, see the documentation below._

## Links

- OpenClaw MCP documentation: https://docs.openclaw.ai/tools/mcp
- This guide on the eContract site: https://econtract.online/mcp/openclaw
- eContract MCP reference (tools, auth, signature placement): https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
