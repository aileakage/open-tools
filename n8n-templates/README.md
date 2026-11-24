# n8n templates

Three n8n workflows that read the free AI Leakage data. Import a file in n8n with **Workflows > Import from file**, follow the yellow note on the canvas, add your own credential, and activate.

| File | What it does | Needs |
|---|---|---|
| `01-slack-terms-watch.json` | Each morning, posts new checked changes to the AI tools you list into a Slack channel. Remembers what it has posted. | Slack credential |
| `02-weekly-email-digest.json` | Every Monday, emails one list of the week's checked changes. Sends nothing in a quiet week. | SMTP credential (or swap in Gmail or Outlook) |
| `03-google-sheets-tool-register.json` | Every Monday, fills in each tool on your Google Sheet register with its AI Leakage profile, last re-read date and last checked change. | Google Sheets credential |

The data: changes checked in the last 90 days with our own one-line summaries, and a facts card per tool. No ratings or scores. CC BY 4.0: keep the link back to each tool's page. General information, not legal advice.
