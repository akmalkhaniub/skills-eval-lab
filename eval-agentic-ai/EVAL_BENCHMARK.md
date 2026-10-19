# Agentic AI Skills Evaluation Benchmark

This evaluation project compares three skills focused on agentic AI workflows and runtime reliability:
1. **`voltagent-workflow`**: Structured ReAct loop, tool orchestration, and adaptive recovery.
2. **`sickn33-guardrails`**: Deterministic loop breaker, prompt injection defense, and safety validation.
3. **`e2b-sandbox-tools`**: Isolated sandbox execution, timeout enforcement, and artifact extraction.

---

## Benchmark Challenge: Autonomous Research & Code Verification Agent

### The Test Prompt
> "Design an autonomous research & verification agent pipeline in Python or TypeScript:
> 1. Agent Architecture: Implements a Planner, Tool Executor, and Critic/Verifier.
> 2. Safety & Guardrails: Limits execution to a maximum of 8 turns, catches cyclic tool errors, and prevents path traversal outside the work directory.
> 3. Execution Engine: Runs a generated code snippet safely, captures stdout/stderr with a 10s timeout, and returns a verified Markdown report with output evidence.
> 4. Error Recovery: If the code snippet fails to compile or run, the agent must catch the exception, reflect on the error log, and attempt exactly one self-repair."

---

## How to Run the Evaluation

1. **Test Candidate A (`voltagent-workflow`)**:
   ```
   git checkout -b test-voltagent
   # Prompt: "Apply the 'voltagent-workflow' skill to design and build the agent architecture in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: voltagent implementation"
   ```

2. **Test Candidate B (`sickn33-guardrails`)**:
   ```
   git checkout main
   git checkout -b test-guardrails
   # Prompt: "Apply the 'sickn33-guardrails' skill to design and build the agent architecture in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: sickn33 guardrails implementation"
   ```

3. **Test Candidate C (`e2b-sandbox-tools`)**:
   ```
   git checkout main
   git checkout -b test-sandbox
   # Prompt: "Apply the 'e2b-sandbox-tools' skill to design and build the agent architecture in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: e2b sandbox implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (VoltAgent) | Candidate B (Guardrails) | Candidate C (Sandbox) |
| :--- | :--- | :--- | :--- |
| **Reasoning & Planning Quality** | | | |
| **Tool Calling Safety & Guardrails** | | | |
| **Loop / Hang Prevention** | | | |
| **Self-Correction & Reflection** | | | |
| **Execution Sandboxing & Isolation** | | | |
