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
