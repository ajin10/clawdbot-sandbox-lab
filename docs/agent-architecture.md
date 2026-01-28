# Clawd.bot – Operational Architecture (Conceptual)

## Control Flow

Chat App  
→ Agent (Planner + Tool Router)  
→ Tool Layer (Shell, Files, APIs, Plugins)  
→ Sandbox Runtime (EC2 / Docker / WSL / Dev Container)  
→ External Systems

## Mental Model

- Chat = Control Plane  
- Agent = Decision Layer  
- Tools = Capability Surface  
- Sandbox = Security Boundary  
- External Systems = Blast Radius  

The agent behaves like a long-running service with permissions, not a traditional chatbot.
