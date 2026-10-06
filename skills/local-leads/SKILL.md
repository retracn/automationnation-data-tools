---
name: local-leads
description: Find local businesses as sales leads, with contact details. Use when the user wants a list of businesses of a type in a place (dentists in Austin, plumbers in Leeds), leads with emails or phones, new businesses, businesses without a website, or UK companies with their directors.
---

Use the AutomationNation connector's `find_local_businesses` tool (any country) or `find_uk_business_leads` (UK, adds Companies House directors). Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--search_flights-9279`; match tools by the name in the middle.

1. Confirm the business type, the location and how many leads are needed. Start small (`max_results` 10–20), because each lead visits the business's website and takes time.
2. Use filters that match the user's offer: `without_website_only` for web design, `opened_within_days` for new businesses, review counts for size.
3. Present a table with name, category, city, phone, email, website, rating and lead score, and explain the scoring briefly.
4. If a run is still going when the tool returns, use `get_run_results` with its `run_id` to fetch the rest.
5. Remind the user that business contact data is subject to privacy and marketing law (for example GDPR and PECR in the UK): contact businesses, not individuals, and include an opt-out.

Leads cost $0.03 each (UK leads $0.05) on the user's Apify account.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
