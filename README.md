# Follow On Tours — MCP Server

**Bespoke cricket travel, powered by AI. Search tours, explore destinations, check match schedules, and submit enquiries — all from your AI assistant.**

[![MCP](https://img.shields.io/badge/MCP-Streamable%20HTTP-blue)](https://modelcontextprotocol.io)
[![Status](https://img.shields.io/badge/Status-Live-brightgreen)]()

## What is this?

Follow On Tours is an AI-powered bespoke cricket travel broker with two decades of experience. This MCP server lets any AI assistant — Claude, ChatGPT, Cursor, or any MCP-compatible client — connect directly to our platform.

**Endpoint:** `https://www.followontours.com/api/mcp`

**Transport:** Streamable HTTP (POST)

**Authentication:** None required (public, read-only tools + rate-limited enquiry submission)

## Available Tools

| Tool | Description |
|------|-------------|
| `get_about` | Learn about Follow On Tours — who we are, how we work, our 21 years of cricket travel experience |
| `search_tours` | Search available cricket tours by destination, dates, series, or format (coming soon) |
| `get_destination_info` | Destination guides — hotels, venues, transfers, visa info, local tips (coming soon) |
| `get_match_schedule` | Upcoming cricket fixtures with dates, venues, and availability (coming soon) |
| `get_tour_modules` | Pre-built tour modules for Australia and other destinations (coming soon) |
| `submit_enquiry` | Submit a qualified travel enquiry for a bespoke proposal (coming soon) |

## Quick Start

### Claude.ai
1. Go to **Settings → Connectors → Add custom connector**
2. Paste: `https://www.followontours.com/api/mcp`
3. Approve the connector
4. Ask Claude: *"Tell me about Follow On Tours"*

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
```
Restart Claude Desktop.

### Any MCP Client
Point your client at:
