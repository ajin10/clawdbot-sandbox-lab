# Experiment 001 – Basic Agent Run (Simulated)

## Objective
Validate that Clawd.bot can:
- Receive messages from a chat interface
- Execute a simple shell command
- Return results back through the chat channel

## Environment (Planned)
- Runtime: AWS EC2 (Ubuntu 22.04) / Docker sandbox
- Chat Interface: Telegram or Slack
- Execution Mode: Reactive (manual trigger, no autonomous loops)

## What I Tried
- Connected agent to a chat interface (Telegram / Slack).
- Issued a basic operational prompt:
  - “List files in the working directory and show disk usage.”
- Expected shell commands:
  - `pwd`
  - `ls -la`
  - `df -h`

## What Worked
- The agent correctly interprets operational intent from natural language.
- Tool invocation follows a clear chain: prompt → shell command → structured output.
- The response pattern aligns with a remote operator model rather than a pure conversational bot.

## What Was Risky / Interesting
- Shell access is inherently high-privilege; without explicit constraints, destructive commands could be executed.
- Filesystem visibility needs scoping (working directory, read-only mounts, or jailed paths).
- The agent behaves more like a service account than a chatbot, which shifts the trust and security model.

## Questions Raised
- How are tool permissions scoped and enforced at runtime?
- Can filesystem access be limited to specific mount points?
- What safeguards prevent accidental or malicious command execution?

