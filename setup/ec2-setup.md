# Clawd.bot on EC2 – Initial Setup

## Goal
Run Clawd.bot in an isolated environment instead of directly on a personal machine.

## Environment
- Cloud: AWS EC2
- OS: Ubuntu 22.04
- Instance Type: (fill in what you used, e.g., t3.small)
- Network: Security group with SSH + outbound internet

## Why EC2
- Isolation from local filesystem
- Easier to tear down and recreate
- Treat the agent like a service, not a local script

## Notes
- Installation steps followed from: https://docs.clawd.bot
- Observations:
  - ...
  - ...
