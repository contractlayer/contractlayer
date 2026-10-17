# Connect your AI client to eContract

Server URL: `https://api.econtract.online/mcp` (Streamable HTTP). Sign in with your eContract account (OAuth 2.1), or send an API key as `Authorization: Bearer cl_live_…`.

| Client | Vendor | Authentication |
|---|---|---|
| [Claude](claude/README.md) | Anthropic | OAuth, API key |
| [Claude Code](claude-code/README.md) | Anthropic | OAuth, API key |
| [ChatGPT](chatgpt/README.md) | OpenAI | OAuth |
| [Codex](codex/README.md) | OpenAI | OAuth, API key |
| [Cursor](cursor/README.md) | Anysphere | OAuth, API key |
| [VS Code (GitHub Copilot)](vscode/README.md) | Microsoft | OAuth, API key |
| [Gemini CLI](gemini-cli/README.md) | Google | OAuth, API key |
| [Muse Code](muse-code/README.md) | Meta | OAuth, API key |
| [OpenClaw](openclaw/README.md) | OpenClaw | OAuth |
| [Hermes Agent](hermes/README.md) | Nous Research | OAuth, API key |

Other MCP clients: point them at the server URL above. Full reference: https://developers.econtract.online/docs/mcp

<!-- Generated from econtract frontend/lib/mcp-agents.ts by scripts/export-mcp-configs.mjs. Do not edit by hand. -->
