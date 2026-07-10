# personal-ai-agent-n8n
A personal AI assistant built with n8n — chat-triggered AI Agent with memory and Gmail tool-calling to autonomously send emails.

## Features
- Chat trigger for conversational input
- OpenAI-powered AI Agent with reasoning
- Simple Memory for conversation context
- Gmail integration as an AI-callable tool (agent decides when to send emails)

## How it works
1. User sends a message via chat trigger
2. AI Agent processes the message using OpenAI + memory
3. If the user requests an email, the agent autonomously calls the Gmail tool
4. Gmail tool sends the email with AI-determined recipient, subject, and body

## Setup
1. Import `workflow.json` into your n8n instance
2. Add your OpenAI and Gmail credentials
3. Activate the workflow and open the chat
