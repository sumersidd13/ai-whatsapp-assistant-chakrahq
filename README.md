# 🤖 AI-Powered WhatsApp Assistant using n8n & ChakraHQ

An AI-powered WhatsApp automation solution built using **n8n**, **OpenAI GPT**, and **ChakraHQ APIs** to automate customer interactions directly within the **WhatsApp Business** application.

Instead of relying on the native WhatsApp node or a separate chat dashboard, this solution integrates WhatsApp through **ChakraHQ**, enabling businesses to continue using their existing WhatsApp Business application while AI automatically handles customer conversations.

---

# 📌 Business Problem

Most WhatsApp automation platforms require businesses to manage customer conversations through a separate dashboard.

This creates additional operational overhead, as support teams must switch between multiple applications to monitor and respond to customer queries.

The objective of this project was to eliminate that dependency by allowing AI-powered conversations while keeping all interactions inside the existing **WhatsApp Business** application.

---

# 🚀 Solution

The workflow receives incoming WhatsApp messages through **ChakraHQ Webhooks**, extracts the required user information, processes the request using an **AI Agent** powered by **OpenAI GPT**, maintains conversation context using memory, and sends the AI-generated response back to the user through the **ChakraHQ API**.

This architecture provides an intelligent customer support experience without requiring any additional dashboard for the business owner.

---

---

# 🏗️ System Architecture

```text
Customer
     │
     ▼
WhatsApp Business
     │
     ▼
ChakraHQ
     │
     ▼
Webhook (n8n)
     │
     ▼
Extract User Details
     │
     ▼
AI Agent (OpenAI GPT)
     │
 ┌───┴────────────┐
 │                │
 ▼                ▼
Prompt Logic   Conversation Memory
 │                │
 └──────┬─────────┘
        ▼
Generate Response
        │
        ▼
HTTP Request
        │
        ▼
ChakraHQ API
        │
        ▼
WhatsApp Business
```

---

# ⚙️ Workflow

1. Customer sends a message using **WhatsApp Business**.
2. **ChakraHQ** forwards the incoming message to an **n8n Webhook**.
3. The workflow extracts the user's phone number, name, and message.
4. The request is processed by an **AI Agent** powered by **OpenAI GPT**.
5. Conversation history is maintained using **Memory** to provide context-aware responses.
6. The AI-generated response is sent back to **ChakraHQ** using an **HTTP Request**.
7. ChakraHQ delivers the response to the customer through **WhatsApp Business**.

---
# ✨ Features

- AI-powered customer support
- WhatsApp Business integration
- ChakraHQ API integration
- Webhook-based event processing
- Prompt engineering
- Conversation memory
- Multi-language support (English, Hindi, Marathi & Hinglish)
- Context-aware conversations
- Menu-driven user interaction
- Modular n8n workflow

# 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Workflow Automation | n8n |
| AI Model | OpenAI GPT |
| Messaging Platform | WhatsApp Business |
| Integration Platform | ChakraHQ |
| APIs | REST API, HTTP Request |
| Trigger | Webhook |
| Memory | Simple Memory |
| AI Components | AI Agent |

# 💼 Business Value

This solution enables businesses to automate WhatsApp conversations without changing their existing communication process.

Key benefits include:

- Continue using the native WhatsApp Business application
- No separate chat dashboard required
- AI-powered automated customer support
- Faster response time
- Reduced manual effort
- Easy integration with existing business workflows

# 🚀 Future Improvements

- Replace Simple Memory with Redis or PostgreSQL for persistent conversation history.
- Integrate vector databases for Retrieval-Augmented Generation (RAG).
- Add human agent handoff.
- Deploy using Docker and cloud infrastructure.
- Integrate CRM platforms for lead management.

# ⚙️ Setup

1. Clone the repository.
2. Import the workflow into n8n.
3. Configure OpenAI API credentials.
4. Configure ChakraHQ API credentials.
5. Update Webhook URL.
6. Activate the workflow.


# 📈 Project Highlights

- Designed an end-to-end AI-powered WhatsApp automation workflow using n8n.
- Integrated WhatsApp Business with ChakraHQ instead of the native WhatsApp node.
- Implemented multilingual support (English, Hindi, Marathi, and Hinglish).
- Built context-aware conversations using AI Agent and conversation memory.
- Automated customer interactions while preserving the existing WhatsApp Business experience.

# 📂 Project Structure

```text
ai-whatsapp-assistant-chakrahq/
│
├── README.md
├── workflow/
│   └── ai-whatsapp-assistant.json
├── screenshots/
├── .env.example
├── .gitignore
└── LICENSE
```

# 🔑 Environment Variables

The following environment variables are required to run the workflow:

| Variable | Description |
|----------|-------------|
| OPENAI_API_KEY | OpenAI API Key |
| CHAKRAHQ_API_KEY | ChakraHQ API Key |
| WEBHOOK_URL | n8n Webhook URL |
