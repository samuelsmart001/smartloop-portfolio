# AI Lead Qualifier

A SmartLoop Automation project by Inioluwa Adebisi.

Every new lead from a website form is read by Claude, scored 0–100 for fit, explained, routed and given a draft reply.

- **Hot leads (70+)**: you get an email alert with the summary and a ready-to-check reply, and the lead is logged.
- **Everyone else**: logged to a Google Sheet nurture list.

## Run it in n8n

1. In n8n, choose **Import from file** and pick `ai-lead-qualifier.n8n.json`.
2. **Claude: qualify lead**: create a *Header Auth* credential with name `x-api-key` and your Anthropic API key as the value.
3. **Alert me: hot lead**: connect your Gmail account.
4. **Log to Google Sheets**: connect Google, paste your sheet URL, and add a tab named `Leads`.
5. Open the form URL from **Website form**, submit a test lead, and check the execution.

Model used: `claude-haiku-4-5-20251001` (fast and low cost). Change it in the HTTP Request body if you prefer.

Live preview page: https://smartloop-portfolio.vercel.app/projects/ai-lead-qualifier/
