# n8n Webhook to Google Sheet Automation

An automated workflow built with n8n that receives incoming webhook data, logs it to Google Sheets, and sends email notifications via Gmail — all without writing a single line of code.

## Workflow Overview

```
Webhook Trigger → Google Sheets (Log Data) → Gmail (Send Notification)
```

## What It Does

1. **Receives data** via HTTP webhook from any external source
2. **Logs the entry** automatically into a Google Sheet with timestamp
3. **Sends an email notification** via Gmail when new data arrives

## Use Cases

- Contact form submissions → auto-logged and notified
- Lead capture from landing pages → stored in Google Sheets instantly
- IoT or app events → tracked and alerted via email
- Any HTTP-triggered automation → Google Sheets + email pipeline

## Tech Stack

- **n8n** — workflow automation platform
- **Webhook** — HTTP trigger node
- **Google Sheets** — data storage and logging
- **Gmail** — email notification delivery

## Workflow Nodes

| Node | Type | Purpose |
|------|------|---------|
| Webhook | Trigger | Receives incoming HTTP requests |
| Append or Update Row | Google Sheets | Logs timestamp, name, email, message |
| Send a message | Gmail | Sends notification email on new entry |

## How to Use

### Option 1: Import to your n8n instance
1. Download `workflow.json` from this repo
2. Open your n8n instance
3. Click **Import** → select the JSON file
4. Connect your Google Sheets and Gmail credentials
5. Activate the workflow

### Option 2: Test the webhook
Send a GET request to your webhook URL with query parameters:
```
https://your-n8n-instance/webhook/your-path?name=John&email=john@example.com&message=Hello
```

## Setup Requirements

- n8n account (cloud or self-hosted)
- Google account with Sheets and Gmail access
- OAuth2 credentials configured in n8n

## Result

- ✅ Data automatically logged to Google Sheets
- ✅ Email notification sent on every new entry
- ✅ Fully automated — zero manual intervention required

## Skills Demonstrated

- n8n workflow development
- Webhook integration and HTTP triggers
- Google Sheets API integration
- Gmail automation via OAuth2
- No-code/low-code automation architecture

## Author

**Rizqi Alfatah**  
AI Automation Specialist | RLHF & Data Annotation Expert  
[Upwork](https://upwork.com) | [LinkedIn](https://linkedin.com/in/rizqialfatah)
