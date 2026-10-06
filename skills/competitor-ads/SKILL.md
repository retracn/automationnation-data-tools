---
name: competitor-ads
description: See the Google ads a company runs and what they say. Use when the user asks about a competitor's ads, ad copy, landing pages, how long ads have been running, ad creative inspiration, or PPC and brand research on Google Search, YouTube or Display.
---

Use the AutomationNation connector's `get_advertiser_ads` tool (Google Ads Transparency Center). Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--search_flights-9279`; match tools by the name in the middle.

1. Pass the competitor's website domain (most complete: every ad linking to it, whichever advertiser account runs it), name or advertiser ID. Set `region` for one country and `format` for text, image or video ads.
2. Keep `include_ad_content` on to get headlines, texts and landing pages.
3. Analyse rather than list: the ads running longest (`daysShown`) are usually the ones that work. Group the ads by offer, message angle and landing page, and quote two or three strong examples.
4. Finish with what the user could test: angles the competitor uses that the user doesn't, and gaps nobody covers.

Ads cost $1 per 1,000 on the user's Apify account.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
