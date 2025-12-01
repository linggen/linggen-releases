# 🚀 Linggen Releases

<p align="left">
  <img src="assets/logo.svg" alt="Linggen logo" width="80" />
</p>

**Linggen — your AI memory layer for code.**  
This repository hosts **pre-built Linggen desktop app binaries** (e.g., `.dmg`, `.deb`) for end-user installation.  
It is **not** the main source code repository.

---

## 🔍 What is Linggen?

Linggen is a **memory + intent layer for AI coding tools** such as Cursor, VS Code, ChatGPT, Claude, and local LLMs.  
It automatically supplies the right context so your AI can reason more deeply about your project.

### Key capabilities

- **Local-first, privacy-first**  
  All code, embeddings, profiles, and memory stay on your machine unless you explicitly enable cloud features.

- **Long-term project memory**  
  Remembers your project architecture, decisions, patterns, and personal preferences over time.

- **Smarter prompts with less typing**  
  You type short instructions; Linggen injects the correct context (code, docs, history, memory) before sending to the AI.

---

## 📦 Downloads & Installation

1. Visit the **[Releases](../../releases)** page of this repository.
2. Download the binary for your OS and architecture (e.g., `Linggen-macos-arm64.dmg`, `Linggen-linux-x86_64.deb`).
3. Install as a normal desktop application.
4. Launch **Linggen** — the app starts a local backend and opens the UI in your browser: http://localhost:8787

---

## 🔌 Using Linggen in Cursor (MCP)

1. Open **Cursor → Settings → MCP**
2. Add a new MCP server:
   - **Name:** `linggen`
   - **URL:** `http://localhost:8787/mcp/sse`
3. Save the configuration.
4. Ensure the Linggen app is running locally.
5. Use Cursor’s MCP features — Cursor will communicate directly with Linggen for context & memory.

---

## 🔐 Privacy & Licensing

- Linggen is **local-first and privacy-focused**.  
  Your code, memories, and embeddings remain on your own machine by default.

- The software is **proprietary**.  
  All rights reserved. Unauthorized redistribution, modification, hosting, or resale are **strictly prohibited**.

- Usage requires a valid license agreement.

For licensing, team deployment, or general inquiries, contact:  
📧 **linggen77@gmail.com**
