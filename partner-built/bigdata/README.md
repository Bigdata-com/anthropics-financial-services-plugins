# Bigdata.com Plugin

This plugin brings [Bigdata.com](https://bigdata.com)'s financial research and market intelligence directly into your AI workflow. It automates research workflows and creates professional deliverables using Bigdata.com MCP tools — company briefs, earnings analysis, risk assessments, and macro economics research.

The skills are built on open standards (MCP) and are designed to work across AI platforms and agent frameworks. While the plugin follows the Claude Cowork standard, all skills and the underlying data layer are platform-agnostic.

These skills are starting points. We encourage you to adapt the prompts, outputs, and workflows to fit your firm's specific processes, templates, and data needs.

## Skills Contained

### Public Company Analysis
**Requires**: [Bigdata.com](https://bigdata.com) subscription or API key

- **Company Briefs** — 30-day development summaries with categorized news and investment implications
- **Earnings Previews** — Pre-earnings analysis with bull/bear cases and key metrics to watch
- **Earnings Digests** — Post-earnings breakdowns with surprises, guidance analysis, and analyst reactions
- **Risk Assessments** — Comprehensive risk profiles with likelihood/impact ratings from SEC filings and news

**Example prompts**:
- "Create a company brief for NVIDIA"
- "Earnings preview for Apple"
- "Risk assessment for Tesla"

### Macro Economics Analysis
**Requires**: [Bigdata.com](https://bigdata.com) subscription or API key

- **Sector Analysis** — Performance, valuations, themes, sub-industries, catalysts
- **Country Profiles** — GDP, inflation, policy, calendar, market implications
- **Country-Sector Analysis** — Macro view of a specific sector within a country
- **Sector Comparisons** — Relative value, rotation signals, cycle positioning
- **Thematic Research** — AI, energy transition, deglobalization, rates
- **Regional Allocation** — G7/G20 comparisons, currency, cross-asset views

**Example prompts**:
- "Analyze the US technology sector"
- "Economic outlook for Germany"
- "Macro analysis of financials in India"
- "Compare G7 economic outlooks"

## MCP Tools

| Tool | Description |
|------|-------------|
| `bigdata_search` | Search for insights across news, filings, transcripts, podcasts, expert interviews, research, and uploaded documents |
| `find_companies` | Identify a public or private company by name and retrieve its Knowledge Graph ID |
| `bigdata_events_calendar` | Returns the corporate earnings calendar and conference call schedule |
| `bigdata_company_tearsheet` | Comprehensive company tearsheet with financial data, market intelligence, and analyst coverage |
| `bigdata_country_tearsheet` | Country economic snapshot with upcoming calendar events, recent releases, market indices, and currencies |

## How to Use

### In Cowork

You'll need a paid Claude plan (Pro, Max, Team, or Enterprise) and the Claude Desktop app for macOS or Windows.

1. Open Claude Desktop and navigate to the **Cowork** tab
1. Click **Customize with Plugins**
1. In Browse Plugins, select **Personal**
1. Click the **plus sign "+"** to add the plugin
1. Authenticate with your Bigdata.com credentials when prompted

Once installed, skills activate automatically when relevant — just describe what you need in natural language.

For the Claude Official Connector (OAuth), see the [Claude MCP Integration guide](https://docs.bigdata.com/mcp-reference/oauth-integrations/claude-mcp-integration).

### In Claude Desktop (individual skills)

1. Open **Settings**
1. Navigate to **Capabilities > Skills**
1. Click **Add**
1. Upload the skill file(s) from this repository

Alternatively, download the pre-built `.skill` file from the [Financial Research Analyst releases](https://github.com/Bigdata-com/skills-financial-research-analyst/releases).

### In Claude Code

```bash
claude plugins add bigdata
```

### With API Key (Cursor, generic hosts)

Configure the Bigdata.com Remote MCP in any MCP-compatible host:

```json
{
  "mcp.bigdata.com": {
    "url": "https://mcp.bigdata.com/",
    "headers": {
      "x-api-key": "<your_api_key>"
    }
  }
}
```

Create or manage API keys at [platform.bigdata.com/api-keys](https://platform.bigdata.com/api-keys).

### Other Platforms

The skills in this repository are markdown files. Any AI platform that supports custom instructions, system prompts, or knowledge file uploads can use them.

- **ChatGPT**: Paste skill content into Custom Instructions or upload as a knowledge file. See [ChatGPT MCP Integration](https://docs.bigdata.com/mcp-reference/oauth-integrations/chatgpt-mcp-integration).
- **Microsoft Copilot**: Paste skill content into a custom prompt or system instruction. See [Copilot MCP Integration](https://docs.bigdata.com/mcp-reference/oauth-integrations/microsoft-copilot-mcp-integration).

## Requirements

- [Bigdata.com](https://bigdata.com) subscription or API key for accessing financial data, news, filings, and analyst estimates
- For API key setup, see [Generic Integration with API Key](https://docs.bigdata.com/mcp-reference/api-integrations/mcp-api-integration)
- For Claude OAuth connector, see [Claude MCP Integration](https://docs.bigdata.com/mcp-reference/oauth-integrations/claude-mcp-integration)

## License

Licensed under the Apache 2.0 License. See [LICENSE](../../LICENSE) for details.

Generated outputs and data are not guaranteed to be correct. **Always verify outputs generated by an LLM for correctness.**
