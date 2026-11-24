# AI Leakage open tools

Free, read-only tools built on the public data from [AI Leakage](https://aileakage.com/?utm_source=github&utm_medium=readme), a New Zealand publication that reads AI vendors' own documents (terms, privacy pages, pricing, subprocessor lists) and dates every change it checks.

Everything here is general information, not legal advice. There are no ratings or scores in this data.

## What is here

| Folder | What it does |
|---|---|
| [`n8n-templates/`](n8n-templates/) | Three n8n workflows: post AI tool terms changes to Slack, a weekly changes digest by email, and an AI tool register kept up to date in Google Sheets. |
| [`mcp/`](mcp/) | How to connect an AI assistant to the read-only AI Leakage facts server (Model Context Protocol). |
| [`msp-tenant-script/`](msp-tenant-script/) | A read-only PowerShell script for IT providers: which AI apps have been added to a Microsoft 365 tenant you manage. |

## The data

| Address | What |
|---|---|
| `https://aileakage.com/wp-json/ail/v1/changes` | JSON: changes checked in the last 90 days, newest first. Add `?tool=<slug>` for one tool. |
| `https://aileakage.com/wp-json/ail/v1/changes.rss` | The same as RSS, for Slack, Teams, feed readers. |
| `https://aileakage.com/wp-json/ail/v1/tools` | JSON: a facts card for every tool covered (profile address, last full re-read, last checked change). |
| `https://aileakage.com/wp-json/ail/v1/tools/<slug>` | One facts card. |

Each change has our own one-line summary (never the vendor's text), the date, the address of our profile for the tool, and the vendor's page where we can pin it to one address.

**Licence:** the data is [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit "AI Leakage (aileakage.com)" and keep the link to each tool's page. The code in this repository is MIT licensed.

**Stable addresses:** the `v1` addresses keep the same shape. If the shape ever has to change, it will be a new `v2` address and `v1` will keep working.

## Questions and problems

Please open an issue in this repository.
