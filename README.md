# Event Growth OS — WebMCP MVP

Agent-native event discovery and human-approved outreach for the WebMCP Challenge.

## MVP
- Deterministic seeded social conversations for a reliable demo.
- Relevance / intent scoring UI.
- AI-style contextual response drafts with explicit non-deceptive positioning.
- Human approval gate before outreach.
- WebMCP Imperative API tools registered through `document.modelContext.registerTool` when supported.
- Stateful tool execution: WebMCP tool calls mutate the same application state and re-render the dashboard.
- Tools: `get_campaign`, `find_relevant_conversations`, `analyze_conversation`, `draft_response`, `request_human_approval`, `record_outcome`.

## Run
npm install
npm run dev

For Chrome local WebMCP testing, enable `chrome://flags/#enable-webmcp-testing` and relaunch Chrome.
