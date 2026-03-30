# Contributing to ecom-mcp-servers

Thanks for helping build the definitive directory of official MCP servers for eCommerce. Every contribution makes this resource more useful for brand owners and agencies.

## Inclusion Criteria

This directory only includes **official, first-party MCP servers** — built and maintained by the company that owns the platform. Community-built and third-party servers are not included.

To qualify, a server must be:

- **Published by the platform company itself** (e.g., Stripe's MCP server is built by Stripe)
- **Publicly available** with documentation or a public repository
- **Actively maintained** by the platform team

Servers built by third-party developers, agencies, integration platforms (e.g., Pipedream wrappers), or CData connectors do not qualify, even if they are well-built. The goal is to provide a trusted, authoritative list that eCommerce teams can rely on.

## How to Submit a New MCP Server

Open a pull request that adds the server entry to the appropriate category section in `README.md`.

### Required Information

Every entry must include:

| Field | Description |
|-------|-------------|
| **Server Name** | Clear, recognizable name |
| **One-line description** | What the server does in plain language |
| **Built by** | The platform company that built it |
| **Links** | GitHub repo URL, docs URL, or both |
| **Auth** | How authentication works (API Key, OAuth, None, etc.) |
| **Status** | `Production`, `Beta`, `Open Beta`, `Developer Preview`, or `Experimental` |
| **Capabilities** | 2-4 bullet points describing key features |

### Entry Format Template

Use this exact format when adding a server:

```markdown
### Server Name

> One-line description of what this server does.

- **Built by:** Company Name
- **Links:** [GitHub](url) | [Docs](url)
- **Auth:** API Key / OAuth / None
- **Status:** Production / Beta

**Capabilities:**
- Capability one
- Capability two
- Capability three
```

### Choosing the Right Category

Place your entry in the most specific category that fits. If a server spans multiple categories, place it in the category that best represents its primary use case and note the breadth in the description.

If no existing category fits, propose a new one in your PR description.

## Pull Request Process

1. **Fork** the repository
2. **Create a branch** with a descriptive name (`add-shipstation-mcp`, `fix-klaviyo-link`)
3. **Make your changes** following the entry format above
4. **Open a PR** with a clear title and brief description of what you're adding or changing
5. **One server per PR** is preferred, but batching related additions is fine

PRs are reviewed for:
- **Official status** — the server must be built by the platform company itself
- **Accuracy** of information (links work, auth method is correct, status is honest)
- **Proper formatting** matching the existing style
- **Correct category** placement
- **No duplicate** entries

## What About Community Servers?

Community-built MCP servers are valuable, but they are outside the scope of this directory. If you've built a third-party MCP server for an eCommerce platform, consider listing it on [mcp.so](https://mcp.so), [glama.ai](https://glama.ai), or the [MCP servers repository](https://github.com/modelcontextprotocol/servers).

## Reporting Broken Links or Outdated Info

If you find a broken link, deprecated server, or outdated information:

1. **Open an issue** with the title: `[Broken/Outdated] Server Name`
2. Include:
   - Which server entry is affected
   - What's wrong (broken link, repo archived, auth changed, etc.)
   - Corrected information if you have it

Or just open a PR with the fix directly.

## Updating the Stats

When adding or removing servers, update:
- The stats line in the header (total count and category count)
- The summary table at the bottom of the README

## Questions?

Open an issue or reach out to [@hamzashahbaz](https://github.com/hamzashahbaz).
