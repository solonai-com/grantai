<p align="center">
  <img src="https://solonai.com/grantai-logo.svg" alt="GrantAi" width="80" height="80">
</p>

<h1 align="center">GrantAi</h1>

<p align="center">
  <strong>Infinite Memory for AI</strong><br>
  Local. Private. Secure.
</p>

<p align="center">
  <a href="https://solonai.com/grantai">Website</a> •
  <a href="https://solonai.com/grantai/download">Download</a> •
  <a href="https://solonai.com/pricing">Pricing</a> •
  <a href="https://solonai.com/help/grantai">Documentation</a>
</p>

---

## What is GrantAi?

GrantAi gives your AI tools persistent memory that runs 100% locally on your machine.

- **12ms Recall** — Sub-second context retrieval across all sessions
- **100% Local** — Your data never leaves your machine
- **AES-256 Encrypted** — Secure at rest, zero data egress
- **Multi-Client** — Claude Code, Cursor, VS Code, and any MCP client share one brain

## Quick Start

### macOS / Linux (Native)

```bash
# 1. Download from https://solonai.com/grantai/download
# 2. Extract and install
./install.sh YOUR_LICENSE_KEY

# 3. Restart your AI tool (Claude Code, Cursor, etc.)
```

### Docker (All Platforms)

```bash
docker pull ghcr.io/solonai-com/grantai-memory:1.8.5
```

Add to your Claude Desktop config (`~/.config/Claude/claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "grantai": {
      "command": "docker",
      "args": ["run", "-i", "--rm", "--pull", "always",
               "-v", "grantai-data:/data",
               "-e", "GRANTAI_LICENSE_KEY=YOUR_KEY",
               "ghcr.io/solonai-com/grantai-memory:1.8.5"]
    }
  }
}
```

## Supported Platforms

| Platform | Method | Status |
|----------|--------|--------|
| macOS (Apple Silicon) | Native | ✅ |
| Linux (x64) | Native | ✅ |
| Windows | Docker | ✅ |
| All Platforms | Docker | ✅ |

## MCP Tools

GrantAi provides these tools to your AI:

| Tool | Description |
|------|-------------|
| `grantai_infer` | Query memory for relevant context |
| `grantai_teach` | Store content for future recall |
| `grantai_learn` | Import files or directories |
| `grantai_health` | Check server status |
| `grantai_summarize` | Store session summaries |
| `grantai_project` | Track project state |
| `grantai_snippet` | Store code patterns |
| `grantai_git` | Import git commit history |

## Pricing

- **Free Trial** — 14 days, no credit card required
- **Personal** — $29/month or $299/year
- **Team** — $25/seat/month

[View full pricing →](https://solonai.com/pricing)

## Documentation

- [Installation Guide](https://solonai.com/help/grantai)
- [FAQ](https://solonai.com/pricing#faq)
- [Troubleshooting](https://solonai.com/help/grantai#troubleshooting)

## Support

- **Issues** — [Open an issue](https://github.com/solonai-com/grantai/issues)
- **Email** — support@solonai.com

## License

GrantAi is proprietary software. See [Terms of Service](https://solonai.com/grantai/terms).

---

<p align="center">
  <a href="https://solonai.com/grantai">Get Started →</a>
</p>
