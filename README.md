# AutomationNation Data Tools for Claude

Give Claude live web data: Google Flights and Hotels prices, Google Shopping, News, Jobs and Trends, YouTube transcripts, local business leads, competitors' Google ads, App Store and Google Play reviews, and AI-search visibility. The plugin connects Claude to the AutomationNation MCP server and adds skills that teach Claude when and how to use it.

## Use it

Ask in plain English, for example:

- "Find nonstop flights from London to New York on 12 December and a 4-star hotel in Midtown for three nights."
- "Summarise this YouTube video with timestamps for the key points."
- "How has search interest in electric bikes changed in the UK this year, and what's in the news about them?"
- "Show me the Google ads hubspot.com is running and which ones have run longest."
- "Find 20 dentists in Austin without a website, with phone numbers."
- "Do Google AI Overviews, Gemini and Claude recommend Notion for team wikis, and who do they recommend instead?"

## Skills

| Skill | Use it for |
|---|---|
| travel-search | Flight fares and hotel prices for your dates |
| youtube-research | Summaries, quotes and search inside YouTube videos, channels and playlists |
| market-research | Google Trends, trending searches, product prices, news and job demand |
| competitor-ads | Competitors' Google ads, copy and landing pages |
| local-leads | Local business leads with contact details, worldwide or UK with directors |
| ai-visibility-audit | Whether AI assistants and Google AI Overviews mention and cite a brand |

## Install

**Claude Code:**

```
/plugin marketplace add retracn/automationnation-data-tools
/plugin install automationnation-data-tools@automationnation
```

Then run `/mcp`, choose **automationnation** and sign in with your Apify account.

**Claude.ai and Claude Desktop:** add the connector under Settings → Connectors → Add custom connector, with the URL `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server`, and sign in with Apify.

A free Apify account works and includes monthly credit; sign up at console.apify.com/sign-up.

## Data and cost

When Claude uses a tool, the plugin sends the tool's inputs (for example a flight route, a search query, a video URL or a brand name) through Apify's MCP server (mcp.apify.com) to AutomationNation's Actors, which run on your Apify account. Results come back to Claude. The plugin stores nothing itself. Apify processes the data under its privacy policy (apify.com/privacy-policy).

Each tool call is billed per result on your Apify account, for example $0.20 per 1,000 flights, $1 per 1,000 hotels or products, $1.50 per 1,000 YouTube transcripts and $0.03 per business lead. Every call carries a spending cap.

## Support

Questions, bugs or feature requests: open an issue at github.com/retracn/automationnation-data-tools/issues. The MCP server's source is at github.com/retracn/automationnation-mcp. MIT licensed.
