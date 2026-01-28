# Clawd.bot Runtime Overview (Planned)

## Goal
Run Clawd.bot as an isolated service rather than a local script.

## Target Runtimes
- AWS EC2 (primary sandbox)
- Docker container (local reproducibility)
- WSL / Dev Containers (developer environments)

## Rationale
- Isolation from host filesystem
- Controlled network egress
- Easier teardown and rebuild
- Clear separation between agent and personal machine

## Future Work
- Dockerfile for agent runtime
- docker-compose for local sandbox
- Infrastructure-as-code for EC2 provisioning
