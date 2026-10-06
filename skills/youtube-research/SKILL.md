---
name: youtube-research
description: Read, summarise, quote or search inside YouTube videos. Use when the user shares a YouTube link, asks what a video, channel or playlist says, wants a summary, key points, quotes with timestamps, or wants to compare what several videos say.
---

Use the AutomationNation connector's `get_youtube_transcripts` tool. Through Apify's hosted connector each tool name carries a prefix and a short suffix, for example `automati--data-tools-mcp-server--search_flights-9279`; match tools by the name in the middle.

1. Pass the video URLs or IDs (up to 10), or a channel or playlist URL with `max_videos_per_channel` for its latest videos. Set `language` to the language the user wants; use `translate_to` only when they need a translation (it's best effort).
2. Set `include_timestamps` when the user wants quotes, chapters or "where does it say…", so you can cite [mm:ss] positions.
3. Base summaries only on the transcript. Structure them as: one-line takeaway, key points, and notable quotes with timestamps. Say if a video has no captions instead of guessing what it contains.
4. For long transcripts, summarise section by section, keeping the timestamps.

Transcripts cost $1.50 per 1,000 on the user's Apify account; videos without captions are free.

If these tools aren't available, the AutomationNation connector isn't connected: ask the user to add `https://mcp.apify.com/?tools=automationnation/data-tools-mcp-server` as an MCP server or connector and sign in with a free Apify account, then continue.
