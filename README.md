# Personal AI Agent — n8n

> A tool-using AI assistant built with **n8n**, conversational memory, OpenAI, and Gmail integration.

[![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI-AI%20Agent-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Gmail](https://img.shields.io/badge/Gmail-Tool%20Integration-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](https://gmail.com/)

## Overview

This project demonstrates a practical **AI-agent workflow** in n8n. A user interacts through a chat trigger, the agent maintains conversational context, and Gmail is exposed as a callable tool for email-related requests.

## Architecture

```text
User
  ↓
Chat Trigger
  ↓
AI Agent ─────→ Simple Memory
  │
  └───────────→ Gmail Tool
                    ↓
                 Email
```

## Key Capabilities

- Conversational chat trigger
- OpenAI-powered AI Agent
- Short-term conversational memory
- Tool calling through Gmail
- Agent-driven email composition
- n8n workflow orchestration

## Workflow

1. The user sends a message through the chat trigger.
2. The AI Agent interprets the request and uses conversation memory for context.
3. When an email action is requested, the agent can invoke the Gmail tool.
4. Gmail sends the resulting message using the recipient, subject, and body determined by the workflow.

## Tech Stack

| Layer | Technology |
|---|---|
| Agent orchestration | n8n |
| AI | OpenAI |
| Memory | n8n Simple Memory |
| Tool integration | Gmail |
| Interface | n8n Chat Trigger |

## Setup

### Prerequisites

- A running n8n instance
- OpenAI credentials
- Gmail credentials with the required permissions

### Installation

1. Clone this repository.
2. Import `workflow.json` into n8n.
3. Configure the OpenAI credential.
4. Configure the Gmail credential.
5. Activate the workflow.
6. Open the chat trigger and test the assistant.

## Security Notes

- Never commit API keys, OAuth secrets, or credential exports.
- Use n8n's credential manager instead of hard-coding secrets in workflow nodes.
- Grant Gmail only the permissions required by the workflow.

## Project Value

This project demonstrates the core building blocks of an **agentic automation system**: an LLM-driven decision layer, memory, tool calling, and workflow orchestration.

## Author

**Pankaj (Tony) Kumar**  
AI Engineer • Full Stack Developer • Generative AI & RAG Specialist

[GitHub](https://github.com/hack2ai) • [LinkedIn](https://www.linkedin.com/in/pankaj-kumar-ab591a216)
