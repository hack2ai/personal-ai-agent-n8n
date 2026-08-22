# Personal AI Agent — n8n

> A tool-using AI assistant built with **n8n**, OpenAI, conversational memory, and Gmail integration.

[![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI-AI%20Agent-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Gmail](https://img.shields.io/badge/Gmail-Tool%20Integration-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](https://gmail.com/)

## Overview

This project demonstrates a practical **agentic automation workflow** in n8n. A user interacts through a chat trigger, the AI agent maintains conversational context, and Gmail is exposed as a callable tool for email-related actions.

The project focuses on the core architecture behind tool-using AI agents rather than presenting a generic chatbot: **LLM reasoning → memory → tool selection → external action → response**.

## Architecture

```text
                         User
                          │
                          ▼
                    Chat Trigger
                          │
                          ▼
                     AI Agent
                    /    │     \
                   /     │      \
                  ▼      ▼       ▼
             OpenAI    Memory   Gmail Tool
                               │
                               ▼
                         Email Action
```

## Agent Execution Flow

```text
1. User sends a request
        ↓
2. Chat Trigger starts workflow
        ↓
3. AI Agent interprets intent
        ↓
4. Memory supplies conversation context
        ↓
5. Agent decides whether a tool is required
        ↓
6. Gmail tool performs the requested email action
        ↓
7. Agent returns the result to the user
```

## Key Capabilities

- Conversational chat trigger
- OpenAI-powered AI agent
- Short-term conversational memory
- Tool calling through Gmail
- Agent-driven email composition
- n8n workflow orchestration
- External-service integration through managed credentials

## Why This Project Matters

Modern AI applications increasingly combine language models with tools and external systems. This workflow demonstrates the fundamental pattern behind those systems without tightly coupling the model directly to application code.

It can serve as a foundation for expanding into:

- Calendar automation
- Task management
- Document retrieval
- RAG pipelines
- Multi-tool agents
- Approval workflows
- Human-in-the-loop automation

## Tech Stack

| Layer | Technology |
|---|---|
| Agent orchestration | n8n |
| AI model | OpenAI |
| Memory | n8n Simple Memory |
| Tool integration | Gmail |
| Interface | n8n Chat Trigger |
| Workflow definition | JSON |

## Repository Structure

```text
personal-ai-agent-n8n/
├── workflow.json       # Importable n8n workflow
└── README.md           # Architecture and setup documentation
```

## Setup

### Prerequisites

- A running n8n instance
- OpenAI credentials
- Gmail credentials with the permissions required by the workflow

### Import the workflow

1. Clone this repository.
2. Open your n8n instance.
3. Import `workflow.json`.
4. Configure the OpenAI credential.
5. Configure the Gmail credential.
6. Review the workflow and tool permissions.
7. Activate the workflow.
8. Open the chat trigger and test the assistant.

## Security & Privacy

Because the workflow can access email functionality, credential scope and tool authorization should be treated as security boundaries.

- Never commit API keys, OAuth secrets, or credential exports.
- Use n8n's credential manager instead of hard-coding secrets.
- Grant Gmail only the minimum permissions required.
- Review tool behavior before enabling the workflow against a real mailbox.
- Do not place sensitive personal information in workflow definitions or test fixtures.
- Add approval/human-in-the-loop controls before allowing higher-impact automated actions.

## Production Extensions

For a production-grade agent, consider adding:

- Explicit tool allowlists
- Human approval before sending sensitive emails
- Audit logging for tool calls
- Structured input/output validation
- Error and retry policies
- Rate limits and usage controls
- Persistent conversation storage
- Evaluation datasets for agent behavior
- Prompt/version management
- Monitoring and alerting

## Project Value

This project demonstrates the core building blocks of an **agentic AI automation system**: LLM-driven intent handling, conversational memory, tool calling, credentialed external actions, and workflow orchestration.

## Author

**Pankaj (Tony) Kumar**  
AI Engineer • Full Stack Developer • Generative AI & RAG Specialist

[GitHub](https://github.com/hack2ai) • [LinkedIn](https://www.linkedin.com/in/pankaj-kumar-ab591a216)
