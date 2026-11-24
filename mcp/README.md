# AI Leakage facts server (MCP)

A read-only [Model Context Protocol](https://modelcontextprotocol.io) server so an AI assistant can look up the same public facts as the AI Leakage feed.

- **Address:** `https://aileakage.com/wp-json/ail/v1/mcp`
- **Transport:** Streamable HTTP (JSON responses). No sign-in, no key.
- **Registry name:** `com.aileakage/ai-tool-facts`

## Tools

| Tool | What it returns |
|---|---|
| `list_tools` | Every AI tool AI Leakage covers, with its profile address. |
| `get_tool_facts` | One tool's facts card: profile address, when the profile was last fully re-read against the vendor's documents, and the date of the last checked change. |
| `recent_changes` | Changes checked in the last 90 days (optionally for one tool), each with our one-line summary, the date and links. |

All three are read only. There are no ratings or scores, and no certificate look-ups.

## What the server keeps

Nothing about your questions. The web server keeps its normal access log, and a counter per IP address for one minute to limit each address to 60 calls a minute. See the [Privacy Policy](https://aileakage.com/privacy-policy/).

## Credit

Data: AI Leakage (aileakage.com), CC BY 4.0. Assistants should cite the `our_page` address given with each answer. General information, not legal advice.
