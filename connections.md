# Connections

The registry of every system your AIOS can reach. This is the Reach layer made visible. Each row is one of the **seven buckets** every business runs on (see `references/the-seven-buckets.md`). `/onboard` fills the tool names from your `context/business-map.md` and intake. You wire the mechanism over time, one tool at a time.

| # | Bucket | Engine | Tool | Mechanism | Auth | Last checked |
|---|---|---|---|---|---|---|
| 1 | Revenue | Growth | _filled by /onboard_ | not yet connected | | |
| 2 | Customer | Growth | _filled by /onboard_ | not yet connected | | |
| 3 | Calendar | Both | _filled by /onboard_ | not yet connected | | |
| 4 | Comms | Both | _filled by /onboard_ | not yet connected | | |
| 5 | Tasks | Fulfillment | _filled by /onboard_ | not yet connected | | |
| 6 | Meetings | Fulfillment | _filled by /onboard_ | not yet connected | | |
| 7 | Knowledge | Both | _filled by /onboard_ | not yet connected | | |

---

## Mechanism options

How the AIOS reaches a tool. Pick the one that fits.

- **mcp**: the tool has an MCP server. The cleanest path when one exists.
- **script**: a small script in `scripts/` that hits the tool's API.
- **export**: no live connection. You drop exported files in and the AIOS reads them.
- **key+ref**: an API key in `.env` plus a `references/{tool}-api.md` guide so the AIOS knows how to call it.
- **not yet connected**: known about, not wired. The default until you do the work.

Wiring a tool means two things, not one. You connect it, and you save `references/{tool}-api.md`: the endpoints, the auth, the request shape. Researched once, saved forever. Next time the AIOS reaches that tool, it reads the guide instead of figuring it out again.

`/audit` reads this file to score engine coverage and how fresh each connection is.
