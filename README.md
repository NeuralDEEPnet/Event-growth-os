# Event Growth OS — Live WebMCP Research

Agent-native event intelligence for the WebMCP Challenge.

## What changed

This version deliberately does **not** pre-compile social conversations. The WebMCP agent can:

1. Load the live event brief.
2. Search the live web through a server-side Tavily connector.
3. Crawl a useful source discovered by research.
4. Rank sources against the event brief.
5. Export the resulting research to an explicitly supplied email address.

The WebMCP tool handlers update the same visible dashboard state, so tool execution is reflected in the UI.

## WebMCP tools

- `get_event_brief`
- `live_web_research`
- `crawl_source`
- `analyze_research`
- `export_research_email`

External web content is marked as untrusted. Email export is marked as consequential and requires an explicit destination.

## Environment variables

Add these in Vercel Project Settings → Environment Variables, then redeploy:

- `TAVILY_API_KEY` — required for live web search/crawl.
- `RESEND_API_KEY` — required for email export.
- `RESEARCH_FROM_EMAIL` — optional verified sender address for Resend.

Tavily provides Search and Crawl APIs for live web research. Resend provides the server-side email API. API keys are never exposed to the browser.

## Run locally

```bash
npm install
npm run dev
```

For Chrome WebMCP testing, enable `chrome://flags/#enable-webmcp-testing` when required by your Chrome build and relaunch Chrome.
