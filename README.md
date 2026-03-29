# MPP Inspector — Claude Code Plugin

> Inspect, debug, and test [Machine Payments Protocol](https://mpp.dev) endpoints directly from Claude Code.

MPP Inspector is a Claude Code plugin that gives you and Claude full visibility into HTTP 402 payment challenges, endpoint discovery, pricing comparison, receipt validation, and end-to-end payment flow dry-runs — all without leaving your editor.

## Quick Start

### Install from the Claude Code Marketplace

```
/plugin marketplace add amgb20/mpp-inspector-marketplace
/plugin install mpp-inspector@mpp-inspector
```

### Try it immediately

```
/mpp-inspect https://mpp.dev/api/ping/paid
/mpp-scan mpp.dev
/mpp-flow https://mpp.dev/api/ping/paid
```

## Features

### Slash Commands

| Command | What it does |
|---------|--------------|
| `/mpp-inspect <url>` | Parse and verify a 402 challenge from any URL |
| `/mpp-scan <domain>` | Discover MPP endpoints across a domain |
| `/mpp-flow <url>` | Dry-run the full payment flow step by step |

### MCP Tools

Five tools are exposed to Claude so it can reason about MPP autonomously:

| Tool | Description |
|------|-------------|
| `mpp_inspect` | Parse and verify a 402 challenge from any URL |
| `mpp_scan` | Discover MPP endpoints on a domain |
| `mpp_compare` | Compare pricing across multiple endpoints |
| `mpp_validate` | Verify receipts and credentials |
| `mpp_flow` | Dry-run the full payment flow |

### Protocol Skill

A built-in skill gives Claude deep knowledge of the MPP specification — challenge parsing, payment methods (Tempo, Stripe, Lightning, Solana, Card), chain configuration, receipt and credential formats, and common debugging patterns.

### Session Hook

Automatically detects when your project uses MPP-related code and surfaces relevant context at session start.

## Natural Language

You can also just ask Claude:

- *"Inspect the MPP challenge at https://mpp.dev/api/ping/paid"*
- *"Scan mpp.dev for MPP endpoints"*
- *"Run a dry-run payment flow against https://mpp.dev/api/ping/paid"*
- *"Compare pricing between these two MPP endpoints"*

## Also Available As

| Distribution | Command |
|-------------|---------|
| **CLI** | `npx mpp-inspector inspect https://mpp.dev/api/ping/paid` |
| **Global install** | `npm install -g mpp-inspector` |
| **Standalone MCP server** | `claude mcp add --transport stdio mpp-inspector -- npx @mpp-inspector/plugin` |

## Links

- **Source code & documentation**: [github.com/amgb20/MPP-Inspector](https://github.com/amgb20/MPP-Inspector)
- **NPM — CLI package**: [npmjs.com/package/mpp-inspector](https://www.npmjs.com/package/mpp-inspector)
- **NPM — Plugin package**: [npmjs.com/package/@mpp-inspector/plugin](https://www.npmjs.com/package/@mpp-inspector/plugin)
- **MPP Protocol docs**: [mpp.dev/overview](https://mpp.dev/overview)

## Contributing

Contributions are welcome! See the [main repository](https://github.com/amgb20/MPP-Inspector) for issues, discussions, and contribution guidelines.

## License

MIT
