# ClawdBot Sandbox Lab

Exploration of running Clawd.bot in sandboxed environments (EC2, Docker, WSL, Dev Containers) and treating agentic AI as an operational system rather than a simple chatbot.

---

## 🔍 Overview

This project documents hands-on experimentation with **Clawd.bot**, a self-hosted, chat-native AI agent capable of executing real actions such as:

- Running shell commands
- Reading and writing files
- Calling APIs
- Orchestrating multi-step workflows
- Operating persistently inside chat platforms (Slack, Telegram, WhatsApp, etc.)

Unlike traditional LLM chat interfaces, Clawd.bot behaves like a **long-running service with permissions**, making it closer to infrastructure than an application. This repository explores what it means to operate such an agent safely and intentionally.

---

## 🏗 System Architecture

High-level flow:

Chat Apps (Slack / Telegram / WhatsApp)
↓
Clawd.bot “Agent Brain”
↓
Tool Interfaces (Shell, Files, APIs)
↓
Sandbox Runtime (EC2 / Docker / WSL / Dev Container)
↓
Real Systems & Services


The agent is treated as an operational workload, running in isolated environments before being granted access to real resources.

---

## 🔐 Operational Principles

Rather than focusing only on “security”, this project adopts an **AgentOps** mindset:

### 1. Isolate
Run the agent in a VM or container first (EC2, Docker, WSL, Dev Containers).

### 2. Connect
Integrate explicitly with chat platforms and APIs.

### 3. Constrain
Treat each plugin, tool, or API as a permission boundary (similar to IAM roles).

### 4. Observe
Start in reactive mode and log behavior before enabling autonomy.

### 5. Expand
Gradually enable background tasks, scheduling, and proactive workflows.

---

## ⚙ Environments Explored

- AWS EC2 (primary sandbox)
- Docker containers
- WSL (Windows Subsystem for Linux)
- Cursor / VS Code Dev Containers

These provide:
- Filesystem isolation
- Network control
- Reproducibility
- Safer experimentation with autonomous execution

---

## 🧠 Key Learnings

- Agentic AI requires **infrastructure thinking**, not just prompt engineering.
- Plugins and tools are effectively **capability grants**.
- Long-running agents should be treated like microservices.
- The mental model is shifting from *using* AI to *operating* AI.

---

## 🚀 Why This Matters

We are entering a phase where:

> A single engineer can coordinate multiple autonomous agents with real system access.

Understanding isolation, permissions, observability, and gradual autonomy is foundational to safely scaling this paradigm.

---

## 📌 Next Directions

Planned extensions:

- Multi-agent orchestration
- Task scheduling & background execution
- Role-based tool permissions
- Audit logging and trace visualization
- Cost-aware auto-scaling runtimes

---

## 🧩 Tech Stack

- Clawd.bot
- AWS EC2
- Docker
- WSL
- Cursor Dev Containers
- Slack / Telegram APIs
- Linux Shell
- REST APIs

---

## 📄 License

MIT License — see `LICENSE` file for details.
