# ContractLayer

Contract infrastructure for developers and AI agents, by [eContract](https://econtract.online).

Let an AI agent prepare a contract, send it for e-signature, follow up and archive the signed PDF, while every signature stays with a real person.

## MCP server

```text
https://api.econtract.online/mcp
```

Streamable HTTP. Sign in with your eContract account (OAuth 2.1) or send an API key as `Authorization: Bearer cl_live_…`. Listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=online.econtract%2Fmcp) as `online.econtract/mcp` ([`server.json`](server.json)).

| Tool | What it does |
|---|---|
| `send_contract` | Create a contract from a PDF/DOCX (inline, link or template) and send it to the signers, in order or in parallel; place each signature next to a text with `signatureAnchor` |
| `list_contracts`, `get_contract` | What is waiting, who has signed, what comes next |
| `get_signing_links`, `send_reminder`, `void_contract` | Share personal signing links, chase signers, cancel |
| `download_signed_document`, `get_audit_trail` | The signed PDF and the signing evidence |
| `verify_pdf` | Check the digital signatures in any PDF |
| `list_templates`, `get_template`, `analyze_contract` | Templates and an AI summary of a contract |

Agents can prepare, send and follow up, but they can never sign or decline for someone: each signer signs through their own link.

### Connect your client

Configs and steps for each client are in [`mcp/`](mcp/README.md): [Claude](mcp/claude/README.md), [Claude Code](mcp/claude-code/README.md), [ChatGPT](mcp/chatgpt/README.md), [Codex](mcp/codex/README.md), [Cursor](mcp/cursor/README.md), [VS Code](mcp/vscode/README.md), [Gemini CLI](mcp/gemini-cli/README.md), [Muse Code](mcp/muse-code/README.md), [OpenClaw](mcp/openclaw/README.md), [Hermes Agent](mcp/hermes/README.md).

## Repositories

| Repository | What it is |
|---|---|
| [verify-pdf](https://github.com/contractlayer/verify-pdf) | Verify the digital signatures in any PDF with one API call, no API key |
| [contract-manager](https://github.com/contractlayer/contract-manager) | REST API examples (Node.js, Python): send a contract, place signatures, share links, download the signed PDF and audit trail |

More examples (agent SDKs, workflow tools) are added alongside the guides on the [eContract blog](https://econtract.online/blog).

## Links

- [eContract](https://econtract.online): free e-signatures with PAdES signatures, RFC 3161 timestamps and a hash-chained audit trail
- [Developer docs](https://developers.econtract.online/docs) and [MCP reference](https://developers.econtract.online/docs/mcp)
- [OpenAPI document](https://api.econtract.online/api/v1/openapi.json)
- [Verify a signed PDF](https://econtract.online/verify)

## License

MIT
