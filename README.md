# Federal Grant Evidence MCP

Federal Grant Evidence is an independent UtilityHouse product for source-backed pursuit screening of U.S. federal grant opportunities. It finds current Grants.gov records, compares a bounded non-personal organization profile with cited hard gates, and can return a versioned award-history evidence pack when the required official evidence is complete.

It does not determine legal eligibility, predict awards, draft applications, or submit applications. It is not affiliated with Grants.gov or the U.S. government.

## Remote MCP endpoint

`https://utilityhouse.xyz/mcp`

Advertised tools:

- `search_federal_grants` — free discovery from current official records.
- `analyze_federal_grant` — free cited hard-gate preview.
- `get_federal_grant_evidence_pack` — complete versioned pack when available.

The paid tool has a disclosed USD 0.09 production launch price, but the current public payment rail is Base Sepolia testnet. Test USDC has no real monetary value, and mainnet settlement is locked.

## Install

### Agent Plugins clients

This repository implements Agent Plugins 1.0 with a root `plugin.json` and `mcp.json`. Compatible clients can install the repository directly.

### Claude

Add a custom web connector with the endpoint above. In Claude Code:

```sh
claude mcp add --transport http federal-grant-evidence https://utilityhouse.xyz/mcp
```

### Gemini CLI

```sh
gemini extensions install https://github.com/tytutueh13-sudo/federal-grant-evidence-mcp
```

### VS Code, GitHub Copilot, and Cursor

Install this Agent Plugin where supported, or add the Streamable HTTP endpoint as a remote MCP server named `federal-grant-evidence`.

## Documentation

- Product: https://utilityhouse.xyz/
- MCP contract: https://utilityhouse.xyz/developers
- Reproducible sample: https://utilityhouse.xyz/sample
- Data status: https://utilityhouse.xyz/data
- Privacy: https://utilityhouse.xyz/privacy
- Terms: https://utilityhouse.xyz/terms
