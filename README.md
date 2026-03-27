# MPP Inspector — Claude Code Plugin Marketplace

Inspect, debug, and test [Machine Payments Protocol](https://mpp.dev) endpoints directly from Claude Code.

## Install

```
/plugin marketplace add amgb20/mpp-inspector-marketplace
/plugin install mpp-inspector@mpp-inspector
```

## What you get

### Slash commands

| Command | Description |
|---------|-------------|
| `/mpp-inspect <url>` | Parse and verify a 402 challenge from any URL |
| `/mpp-scan <domain>` | Discover MPP endpoints on a domain |
| `/mpp-flow <url>` | Dry-run the full payment flow |

### 5 MCP tools (used by the commands above)

| Tool | Description |
|------|-------------|
| `mpp_inspect` | Parse and verify a 402 challenge from any URL |
| `mpp_scan` | Discover MPP endpoints on a domain |
| `mpp_compare` | Compare pricing across multiple endpoints |
| `mpp_validate` | Verify receipts and credentials |
| `mpp_flow` | Dry-run the full payment flow |

### MPP protocol skill

A built-in skill that gives Claude deep understanding of the MPP spec including challenge parsing, payment methods (Tempo, Stripe, Lightning, Solana, Card), chain configuration, receipt/credential formats, and debugging patterns.

### Session hook

Automatically detects when your project uses MPP-related code and surfaces relevant context.

## Try it

After installing, use the slash commands:

```
/mpp-inspect https://mpp.dev/api/ping/paid
/mpp-scan mpp.dev
/mpp-flow https://mpp.dev/api/ping/paid
```

Or ask Claude directly:

- "Inspect the MPP challenge at https://mpp.dev/api/ping/paid"
- "Scan mpp.dev for MPP endpoints"
- "Run a dry-run payment flow against https://mpp.dev/api/ping/paid"
- "Compare pricing between these two MPP endpoints"

## Also available as

- **CLI**: `npx mpp-inspector inspect https://mpp.dev/api/ping/paid`
- **npm**: `npm install -g mpp-inspector`
- **MCP server**: `claude mcp add --transport stdio mpp-inspector -- npx @mpp-inspector/plugin`

## Links

- [NPM CLI package](https://www.npmjs.com/package/mpp-inspector)
- [NPM plugin package](https://www.npmjs.com/package/@mpp-inspector/plugin)
- [Source code](https://github.com/amgb20/MPP-Inspector)
- [MPP Protocol docs](https://mpp.dev/overview)

## License

MIT
