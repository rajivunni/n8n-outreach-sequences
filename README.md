# n8n Outreach Sequences

n8n workflows for automated multi-step outreach campaigns and AI content generation. Pulls leads from Apollo, sends personalised emails via Gmail, handles follow-ups on a schedule, and generates multi-channel content from a single trigger.

## Workflows

### Accounting Firm Outreach - Email 1
Pulls accounting firm contacts from Apollo, normalises them, generates a personalised first email using AI, sends via Gmail, and logs each send to Google Sheets.

**Stack:** Apollo API, Gmail, Google Sheets, n8n batch processing

### Accounting Firm Outreach - Email 2 Follow-up
Runs on a weekday 9am schedule. Reads the outreach sheet, filters contacts due for a follow-up, generates email 2, sends via Gmail, and marks them as sent in the sheet.

**Stack:** Schedule Trigger, Gmail, Google Sheets

### Content Gen - Multi-channel
Single-trigger workflow that generates a full week of content from one input. Produces a blog post, two LinkedIn posts, two X posts, a newsletter section, and a Facebook post using OpenAI. Saves to Google Docs and sends a summary via Gmail.

**Stack:** OpenAI, Google Docs, Gmail, HTTP Request

## Tech Stack

- [n8n](https://n8n.io) - workflow automation
- Apollo - lead sourcing
- OpenAI - content and email generation
- Gmail - sending
- Google Sheets - outreach tracking
- Google Docs - content storage

## Usage

1. Import the `.json` file into your n8n instance via **Workflows > Import from file**
2. Configure credentials: Apollo API key, OpenAI API key, Gmail OAuth, Google Sheets OAuth
3. Update the Campaign Config node with your target niche and sender details
4. Activate the workflow

## About

Built by [Rajiv Unnikrishnan](https://www.rajivunnikrishnan.com) - n8n automation specialist.
