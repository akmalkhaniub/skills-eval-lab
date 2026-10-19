# Security & Vulnerability Audit Skills Benchmark

This evaluation project compares three security-oriented skills:
1. **`owasp-secure-coding`**: Hardening against OWASP Top 10 vulnerabilities (SQLi, IDOR, XSS, CSRF).
2. **`auth-tokens-guard`**: JWT rotation, HttpOnly cookie flags, and session/RBAC validation.
3. **`agent-prompt-defense`**: Indirect prompt injection mitigation and untrusted data boundary fences.

---

## Benchmark Challenge: Secure Document Sharing & Summarization Endpoint

### The Test Prompt
> "Build a secure REST/tRPC endpoint for a **Document Sharing & AI Summarization Service** in TypeScript:
> 1. Ingestion: Accepts a document title, content body (potentially containing malicious payloads/scripts), and visibility level ('private' | 'team').
> 2. Security & IDOR: Verify that the caller has permissions to share or summarize in the target organization. Reject unauthorized IDOR attempts.
> 3. Injection Prevention: Sanitize input against XSS, ensure parameterized database insertion, and prevent indirect prompt injection when sending document content to an LLM summarizer.
> 4. Auth & Rate Limiting: Require valid JWT via HttpOnly cookies and enforce a sliding-window rate limit (10 requests/minute per user)."

---

## How to Run the Evaluation

1. **Test Candidate A (`owasp-secure-coding`)**:
   ```powershell
   git checkout -b test-owasp
   # Prompt: "Apply the 'owasp-secure-coding' skill to implement the endpoint described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: OWASP implementation"
   ```

2. **Test Candidate B (`auth-tokens-guard`)**:
   ```powershell
   git checkout main
   git checkout -b test-auth-guard
   # Prompt: "Apply the 'auth-tokens-guard' skill to implement the endpoint described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: Auth Guard implementation"
   ```

3. **Test Candidate C (`agent-prompt-defense`)**:
   ```powershell
   git checkout main
   git checkout -b test-prompt-defense
   # Prompt: "Apply the 'agent-prompt-defense' skill to implement the endpoint described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: Prompt Defense implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (OWASP) | Candidate B (Auth Guard) | Candidate C (Prompt Defense) |
| :--- | :--- | :--- | :--- |
| **IDOR & Access Control Rigor** | | | |
| **XSS / SQLi Sanitization** | | | |
| **Cookie & Token Lifecycle Security** | | | |
| **Prompt Injection Boundary Fencing** | | | |
| **Rate Limiting & Abuse Defense** | | | |
