# Experiment 002 – Permission Boundaries (Simulated)

## Objective
Reason about how Clawd.bot’s access to shell, files, and APIs should be constrained when running in a sandbox.

## Capability Surface
- Shell execution
- Filesystem read/write
- Network and API calls
- Plugin-based tool access

## Key Observations
- Each enabled tool effectively grants a new capability.
- Without isolation, the agent inherits the full privilege of the runtime user.
- Plugins behave more like IAM roles than simple extensions.

## Risks
- Accidental execution of destructive shell commands.
- Unintended access to sensitive filesystem paths.
- Over-broad API keys enabling lateral movement.

## Operator Takeaway
Treat every tool and plugin as a permission boundary and apply least-privilege by default, similar to cloud service role design.
