---
name: e2b-sandbox-tools
description: Sandboxed code execution, ephemeral container management, and safe external environment integration for AI agents. Use when agents need to run untrusted code, execute scripts, or build interactive artifacts.
---

# Sandboxed Execution & Tooling Skill
**Source:** Inspired by [e2b-dev/awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents)

## Core Directives
1. **Isolated Execution**:
   - Run generated code in disposable sandboxes (Docker, WebAssembly, or E2B cloud containers).
   - Never run untrusted agent-generated code with host admin/root privileges.
2. **Resource Boundaries**:
   - Enforce timeouts (default: 30s) and memory caps (e.g. 512MB) per execution.
   - Stream stdout/stderr in chunks; terminate if runaway output is detected.
3. **Artifact Extraction**:
   - Collect generated images, charts, and data files from the sandbox and save them to a designated artifacts directory.
