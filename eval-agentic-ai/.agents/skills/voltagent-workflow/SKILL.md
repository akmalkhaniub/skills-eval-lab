---
name: voltagent-workflow
description: Autonomous multi-step agent reasoning, tool orchestration, and dynamic recovery loop. Enforces structured Plan-Act-Observe-Reflect cycles for complex problem-solving agents. Use when orchestrating autonomous AI agents.
---

# Autonomous Workflow Skill (VoltAgent Edition)
**Source:** Inspired by [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)

## The ReAct Loop Directives
1. **Plan First**:
   - Decompose ambiguous goals into ordered, finite steps.
   - For each step, determine the expected observation and success indicator.
2. **Tool Selection & Execution**:
   - Validate tool arguments before making tool calls.
   - Run one mutation at a time; never execute multiple blind writes without inspecting intermediate outputs.
3. **Observation & Reflection**:
   - Compare the tool result against expected criteria.
   - If an error or unexpected output is returned, do not repeat the exact same call. Hypothesize the root cause, adjust parameters, or change tools.
4. **Final Synthesis**:
   - Deliver an executive summary citing specific evidence gathered during execution.
