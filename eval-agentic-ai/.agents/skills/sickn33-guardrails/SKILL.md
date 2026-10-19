---
name: sickn33-guardrails
description: Deterministic safety guardrails, prompt injection mitigation, strict validation checkpoints, and cost/token budget limits for autonomous agents. Use when designing safe, production-reliable AI agent architectures.
---

# Agent Guardrails & Reliability Skill
**Source:** Inspired by [sickn33/agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills)

## Core Directives
1. **Input / Output Guardrails**:
   - Sanitize dynamic inputs to prevent indirect prompt injection.
   - Restrict tool parameters using strict schema constraints (e.g. regex on file paths to prevent directory traversal).
2. **Deterministic State & Loop Detection**:
   - Track iteration count; abort if the agent executes > 10 tool calls without state progress.
   - Detect cyclic tool invocations (calling tool A -> error -> calling tool A with same inputs).
3. **Fail-Safe & Human-in-the-Loop**:
   - High-impact operations (database drop, destructive file delete, external payments) require explicit approval or dry-run preview.
   - Maintain full structured audit logs (`timestamp`, `tool_name`, `args`, `result`, `error`).
