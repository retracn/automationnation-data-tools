---
name: market-research
description: Research demand, prices and news for a market, product or topic with live Google data. Use when the user asks what's trending, how interest in something is changing, seasonality, comparing products or brands by search interest, current prices of a product, recent news about a company, or job market demand.
---

Combine the AutomationNation connector's research tools as the question needs. Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--get_google_trends-7d5f`; match tools by the name in the middle:

- `get_google_trends`: interest over time, top regions and rising searches for up to 5 terms. Set `compare` to put terms on one scale, `geo` for a country or region, and `time_range`.
- `get_trending_searches`: what's trending right now in a country.
- `search_google_shopping`: current prices, discounts, stores and ratings for a product in a country.
- `search_google_news`: recent coverage. Use `sort_by: date` and `time` for "latest" questions.
- `search_jobs`: job listings and salaries, as a demand signal for skills or roles.

Work in this order: frame the question, pull the minimum data that answers it, then report findings with numbers and dates (for example "interest up 34% over the last 90 days, peak on 9 September"). Separate what the data shows from your interpretation. Keep `max_results` modest: every call is billed per result on the user's Apify account.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
