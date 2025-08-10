# WhatsApp-Driven Google Drive Assistant (n8n Workflow)
## Overview

### This n8n workflow creates an intelligent assistant that listens to WhatsApp messages and performs various Google Drive actions based on simple text commands. The assistant can list files, delete/move documents, and even provide AI-generated summaries of your files. Features
WhatsApp Integration: Uses Meta's WhatsApp Cloud API as the inbound channel
Google Drive Operations:
- List files in a folder
- Delete specific files
- Move files between folders
- Generate AI summaries of documents
- AI-Powered Summarization: Uses gemini-2.5-pro to create concise document summaries
- Safety Features: Audit logging and confirmation requirements for destructive operations

### Prerequisites
- Meta Developer Account with WhatsApp Business API access
- Google Cloud Project with Drive API enabled
- n8n instance

## Setup Instructions
1. WhatsApp Configuration

Create a Meta Developer account at developers.facebook.com

Set up a WhatsApp Business account and get your:
- Phone Number ID
- WhatsApp Business Account ID
- Permanent Access Token

Configure a webhook URL (your n8n webhook URL) in WhatsApp settings

2. Google Drive Configuration

    Create a project in Google Cloud Console

    Enable the Google Drive API

    Create OAuth 2.0 credentials

    Download the credentials JSON file

3. Gemini Configuration

   sign up to google gemini

   generate an API key


## Command Syntax

Send WhatsApp messages in these formats:

- List files: LIST

- Delete file: DELETE [filename] CONFIRM

- Move file: MOVE [source] [destination]

- Summarize: SUMMARY

- Help: HELP
