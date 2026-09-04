# Federal Grant Evidence MCP

Federal Grant Evidence is an independent UtilityHouse product for source-backed pursuit screening of U.S. federal grant opportunities. It finds current Grants.gov records, compares a bounded non-personal organization profile with cited hard gates, and can return a versioned award-history evidence pack when the required official evidence is complete.

It does not determine legal eligibility, predict awards, draft applications, or submit applications. It is not affiliated with Grants.gov or the U.S. government.

## Free-beta access

`https://grants.utilityhouse.xyz/mcp`

Advertised tools:

- `search_federal_grants` — free discovery from current official records.
- `analyze_federal_grant` — free cited hard-gate preview.
- `get_federal_grant_evidence_pack` — complete versioned pack when available.

All three tools are free during the limited beta. The complete pack is limited to 100 newly released results per UTC day. No wallet, payment authorization, or blockchain transaction is requested. A future paid release is separate and mainnet remains locked.

For aggregate channel attribution, directory and client integrations use equivalent channel-specific endpoints:

| Channel | Endpoint |
|---|---|
| OpenAI / ChatGPT | `https://grants.utilityhouse.xyz/mcp/openai` |
| Claude | `https://grants.utilityhouse.xyz/mcp/claude` |
| Official MCP Registry | `https://grants.utilityhouse.xyz/mcp/registry` |
| Smithery | `https://grants.utilityhouse.xyz/mcp/smithery` |
| Cursor | `https://grants.utilityhouse.xyz/mcp/cursor` |
| Glama | `https://grants.utilityhouse.xyz/mcp/glama` |
| PulseMCP | `https://grants.utilityhouse.xyz/mcp/pulsemcp` |
| Gemini | `https://grants.utilityhouse.xyz/mcp/gemini` |
| GitHub Copilot | `https://grants.utilityhouse.xyz/mcp/copilot` |

Every endpoint exposes the same three tools and the same free-beta behavior. The service stores only aggregate Korea calendar date (Asia/Seoul), channel, tool, outcome, and count. It does not store caller identity, request bodies, organization profiles, result contents, wallet data, or transaction data in usage analytics.

## Install

### Agent Plugins clients

This repository implements Agent Plugins 1.0 with a root `plugin.json` and `mcp.json`. Compatible clients can install the repository directly.

### Claude

Add a custom web connector with the Claude endpoint. In Claude Code:

```sh
claude mcp add --transport http federal-grant-evidence https://grants.utilityhouse.xyz/mcp/claude
```

The repository also includes a validated Claude plugin manifest, remote MCP configuration, and a narrowly scoped tool-routing skill for submission to the official Claude Plugin Directory.

### Gemini CLI

```sh
gemini extensions install https://github.com/tytutueh13-sudo/federal-grant-evidence-mcp --auto-update
```

The repository is also tagged with `gemini-cli-extension` for Gemini's automatic extension-gallery discovery.

### GitHub Copilot in VS Code

[Install Federal Grant Evidence in VS Code](vscode:mcp/install?%7B%22name%22%3A%22federal-grant-evidence%22%2C%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fgrants.utilityhouse.xyz%2Fmcp%2Fcopilot%22%7D)

Or install from a terminal:

```sh
code --add-mcp '{"name":"federal-grant-evidence","type":"http","url":"https://grants.utilityhouse.xyz/mcp/copilot"}'
```

### GitHub Copilot cloud agent

Repository administrators can paste [`copilot-mcp.json`](./copilot-mcp.json) into **Settings → Copilot → MCP servers**. It explicitly allowlists the same three non-destructive tools.

### Other Agent Plugin clients and Cursor

Install this Agent Plugin where supported, or add the matching Streamable HTTP endpoint above as a remote MCP server named `federal-grant-evidence`.

## Documentation

- Product: https://grants.utilityhouse.xyz/
- MCP contract: https://grants.utilityhouse.xyz/developers
- Official MCP Registry API record: https://registry.modelcontextprotocol.io/v0.1/servers?search=xyz.utilityhouse%2Ffederal-grant-evidence
- Public Smithery listing: https://smithery.ai/servers/tytutueh13/federal-grant-evidence
- Reproducible sample: https://grants.utilityhouse.xyz/sample
- Data status: https://grants.utilityhouse.xyz/data
- Privacy: https://grants.utilityhouse.xyz/privacy
- Terms: https://grants.utilityhouse.xyz/terms
