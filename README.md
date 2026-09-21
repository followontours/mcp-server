# Follow On Tours — MCP Server

**Bespoke cricket and golf travel, powered by AI.** Connect any MCP-compatible assistant to live tour data, destinations, golf trips, and financial-protection facts.

[![MCP](https://img.shields.io/badge/MCP-Streamable%20HTTP-blue)](https://modelcontextprotocol.io)
[![Status](https://img.shields.io/badge/Status-Live-brightgreen)]()

## What is this?

Follow On Tours Limited is the **tour operator and package organiser** for every trip it sells — it contracts directly with the traveller and takes payment. **Not a broker, introducer, or agent.** Founded and run by Ian Kerr, with over **17 years** arranging tours to the great grounds and the great courses. Darren Gough MBE is ambassador and shareholder.

Financial protection: **ABTOT bonded, member 5718**. Non-flight packages are bond-protected. Follow On Tours does not hold an ATOL licence and does not sell flights.

This MCP server lets any AI assistant — Claude, ChatGPT, Cursor, or any MCP-compatible client — connect directly to our public read-only tools.

**Endpoint:** `https://www.followontours.com/api/mcp`

**Transport:** Streamable HTTP (POST)

**Authentication:** None required for read tools

**Also:** [llms.txt](https://www.followontours.com/llms.txt) · [catalogue.json](https://www.followontours.com/catalogue.json)

## Available Tools

| Tool | Description |
|------|-------------|
| `get_about` | Who Follow On Tours is, what we sell (bespoke cricket and golf travel), experience, protection, and how the service works |
| `list_tours` | Published cricket tours currently on sale, plus `holdingTours` (announced, not bookable — schedules not confirmed) |
| `list_golf_trips` | Golf trips (Trump portfolio venues hosted with Darren Gough) — enquiry-led, no online price/payment |
| `list_destinations` | Cricket destinations and grounds (bespoke / built to order) |
| `list_cape_town_experiences` | Cape Town day experiences (enquiry-led) |
| `get_protection` | Financial protection statement — tour operator / package organiser, ABTOT 5718 |

## Quick Start

### Claude.ai
1. Go to **Settings → Connectors → Add custom connector**
2. Paste: `https://www.followontours.com/api/mcp`
3. Approve the connector
4. Ask Claude: *"Tell me about Follow On Tours"* or *"List cricket tours"*

### Claude Desktop
Add to `~/Library/Application Support/Claude/claude_desktop_config.json`:
```json
{
  "mcpServers": {
    "followontours": {
      "url": "https://www.followontours.com/api/mcp"
    }
  }
}
