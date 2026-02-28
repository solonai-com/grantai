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

GrantAi is the **shared memory layer** for AI agents.

Coordination frameworks are everywhere — CrewAI, AutoGen, LangGraph. But agents still lose everything when a session ends. Context windows reset. Knowledge evaporates. Each agent starts from zero.

GrantAi solves this:

- **Persistent Memory** — Knowledge survives sessions, accumulates over time
- **Shared Across Agents** — Multiple AI tools read and write to the same brain
- **12ms Recall** — Sub-second retrieval regardless of memory size
- **100% Local** — Your data never leaves your machine
- **AES-256 Encrypted** — Secure at rest, zero data egress

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
| `grantai_capture` | Save conversation turns for continuity |

## Multi-Agent Memory Sharing

Multiple agents can share knowledge through GrantAi's memory layer.

### Writing memories with agent attribution

```python
# Agent 1: Researcher stores findings
grantai_teach(
    content="API rate limit is 100 requests/minute. Auth uses Bearer tokens.",
    source="api-research",
    speaker="researcher"
)

# Agent 2: Coder stores implementation notes
grantai_teach(
    content="Implemented retry logic with exponential backoff in api_client.py",
    source="implementation",
    speaker="coder"
)
```

### Querying memories from specific agents

```python
# Get only what the researcher found
grantai_infer(
    input="API authentication",
    from_agents=["researcher"]
)

# Get everything from all agents
grantai_infer(
    input="API rate limiting"
)
```

### Use cases

| Scenario | How it works |
|----------|--------------|
| **Research → Code** | Research agent stores findings, coding agent retrieves them |
| **Multi-tool workflow** | Cursor for coding, Claude Code for commits — same memory |
| **Session continuity** | Agent picks up where another left off |
| **Team knowledge base** | All agents contribute to shared project context |

### Framework integration

GrantAi works with any MCP-compatible client. Point your agents at the same GrantAi instance:

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

All agents using this config share the same memory volume (`grantai-data`).

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
