# Follow On Tours — MCP Server

**Bespoke sports travel, powered by AI: cricket, golf, rugby, polo and playing tours.** Connect any MCP-compatible assistant to live tour data, indicative prices, destinations, golf trips and financial-protection facts, and request a quote for a traveller.

Registry name: `com.followontours/cricket-travel` (all sports since 1.0.2).

[![MCP](https://img.shields.io/badge/MCP-Streamable%20HTTP-blue)](https://modelcontextprotocol.io)
[![Status](https://img.shields.io/badge/Status-Live-brightgreen)]()

## What is this?

Follow On Tours Limited is the **tour operator and package organiser** for every trip it sells — it contracts directly with the traveller and takes payment. **Not a broker, introducer, or agent.** Founded and run by Ian Kerr, with over **17 years** arranging tours to the great grounds and the great courses. Darren Gough MBE is ambassador and shareholder.

Financial protection: **ABTOT bonded, member 5718**. Non-flight packages are bond-protected. Follow On Tours does not hold an ATOL licence and does not sell flights.

This MCP server lets any AI assistant — Claude, ChatGPT, Cursor, or any MCP-compatible client — connect directly to our public tools. All are read-only except `request_quote`, which emails the traveller to confirm before anything reaches us.

**Endpoint:** `https://www.followontours.com/api/mcp`

**Transport:** Streamable HTTP (POST)

**Authentication:** None

**Also:** [llms.txt](https://www.followontours.com/llms.txt) · [catalogue.json](https://www.followontours.com/catalogue.json)

## Available Tools

| Tool | Description |
|------|-------------|
| `get_about` | Who Follow On Tours is, what we sell (bespoke sports travel: cricket, golf, rugby, polo and playing tours), experience, protection and how it works |
| `list_tours` | Published tours on sale, with what is included, optional extras, payment terms and from-prices; plus trips quoted on request and announced tours not yet on sale |
| `get_price` | Indicative price for a published tour from our own booking engine, for a number of travellers, sharing or single, and a chosen match |
| `list_golf_trips` | Golf trips: the Trump links in Scotland and Ireland, a set-price week in Sri Lanka, and bespoke golf on request. Darren Gough MBE can host on request, subject to his availability |
| `list_destinations` | Countries and sport pages, leading with any tour on sale, plus the grounds we build cricket trips around |
| `list_cape_town_experiences` | Cape Town day experiences (enquiry-led) |
| `get_protection` | Financial protection statement: tour operator and package organiser, ABTOT 5718 |
| `request_quote` | Asks Follow On Tours for a quote on a traveller's behalf. The traveller confirms by email; nothing is booked or charged |

## Quick Start

### Claude.ai
1. Go to **Settings → Connectors → Add custom connector**
2. Paste: `https://www.followontours.com/api/mcp`
3. Approve the connector
4. Ask Claude: *"Tell me about Follow On Tours"* or *"What sports tours are on sale?"*

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
