---
name: travel-search
description: Find live flight fares and hotel prices. Use when the user asks about flights, airfares, the cheapest or fastest way to fly between places, flight times or stops, hotel prices, where to stay, or planning a trip with dates.
---

Use the AutomationNation connector's travel tools: `search_flights` (Google Flights) and `search_hotels` (Google Hotels). Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--search_flights-9279`; match tools by the name in the middle.

1. Get what you need before searching: origin and destination (airport codes or cities), dates (YYYY-MM-DD), number of travellers, and for hotels the city or area plus check-in and check-out. If the user gives only a month, pick sensible dates and say so.
2. Flights: call `search_flights` once per route and date. Set `return_date` for round trips (prices are then round-trip totals), `stops` when the user wants nonstop, and `currency` in the user's currency. Keep `max_results` around 10–15.
3. Hotels: call `search_hotels` with `check_in` and `check_out` so prices are exact. Use `min_rating`, `min_stars` or `max_price_per_night` when the user states a preference.
4. Present a short comparison table: price, airline or hotel, times or rating, stops or distance, and one-line pros and cons. Lead with the best value option, then the cheapest and the fastest or best located.
5. Prices change constantly: say when they were fetched, link the Google Flights or Google Hotels result, and don't present them as bookable quotes.

Each call runs on the user's Apify account and is billed per result (flights $0.20 per 1,000, hotels $1 per 1,000), so avoid large repeated searches unless the user asks.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
