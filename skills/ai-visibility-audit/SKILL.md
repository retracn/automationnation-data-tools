---
name: ai-visibility-audit
description: Check whether AI assistants and Google AI Overviews mention and cite a brand or website. Use when the user asks about AI search visibility, GEO or AEO, whether ChatGPT-style answers recommend them, share of voice in AI answers, which competitors AI recommends, or whether Google AI Overviews cite their site.
---

Use the AutomationNation connector's `check_ai_visibility` (Google AI Overviews, Gemini and Claude) and `check_ai_overview_citations` (Google AI Overviews for given searches) tools. Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--search_flights-9279`; match tools by the name in the middle.

1. Collect the brand, its website, 3–5 competitors and 5–10 questions real customers ask ("best CRM for small business", "X vs Y"). Suggest questions if the user has none.
2. Run `check_ai_visibility` with those prompts and competitors, and `check_ai_overview_citations` for the user's key searches and domain.
3. Report: how often the brand is mentioned and cited per engine, its rank against competitors, which competitors are named instead, the sentiment, and the sources the engines cite.
4. Turn it into actions: the sources the engines lean on (review sites, listicles, YouTube, Reddit) where the brand should appear, and the questions where it is absent.
5. Suggest re-running the same prompts monthly to track the trend.

Each answer checked costs $0.05; AI Overview keyword checks cost $0.04 each (plus $2 per run from 17 November 2026), on the user's Apify account.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
