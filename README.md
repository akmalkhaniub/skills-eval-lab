# Skills Evaluation Lab

A comprehensive multi-project testbed for benchmarking, comparing, and testing AI agent skills across the entire software development lifecycle.

---

## Evaluation Projects Directory

| Project Directory | Domain | Candidates Installed | Evaluation Benchmark |
| :--- | :--- | :--- | :--- |
| **[`eval-ui-ux/`](./eval-ui-ux/)** | UI/UX & Design Systems | `plugin87-ux-ui`<br>`nextlevel-ui-ux-promax`<br>`jakubkrehel-accessibility` | Themeable Metric Card, DTCG tokens, micro-interactions, WCAG 2.2 AAA |
| **[`eval-fullstack/`](./eval-fullstack/)** | Full-Stack Engineering | `minimax-fullstack-dev`<br>`addyosmani-engineering`<br>`bulletproof-architecture` | SaaS Subscription & Feature-Gate, typed contracts, 3-tier layering |
| **[`eval-agentic-ai/`](./eval-agentic-ai/)** | Autonomous Agents | `voltagent-workflow`<br>`sickn33-guardrails`<br>`e2b-sandbox-tools` | Autonomous research agent, ReAct loop, injection guards, container sandbox |
| **[`eval-core-engineering/`](./eval-core-engineering/)** | SOLID & Cloud Platforms | `solid-clean-code`<br>`aws-cdk-serverless`<br>`gcp-cloud-architecture` | Multi-channel invoicing engine, Open/Closed principle, AWS CDK & GCP Run |
| **[`eval-security-audit/`](./eval-security-audit/)** | Security & Auth | `owasp-secure-coding`<br>`auth-tokens-guard`<br>`agent-prompt-defense` | Secure document sharing API, IDOR prevention, JWT rotation, prompt fences |
| **[`eval-testing-qa/`](./eval-testing-qa/)** | Automated Testing & QA | `tdd-vitest-jest`<br>`playwright-e2e`<br>`mutation-property-testing` | Checkout & discount engine, Red-Green TDD, browser E2E, fast-check |
| **[`eval-database-performance/`](./eval-database-performance/)** | Database & Caching | `db-schema-migrations`<br>`query-optimization-indexing`<br>`cache-redis-patterns` | High-throughput activity feed, zero-downtime expand-contract, Redis mutex |
| **[`eval-devops-cicd/`](./eval-devops-cicd/)** | Containers & Pipelines | `docker-container-hardening`<br>`github-actions-workflows`<br>`terraform-iac-platform` | Hardened multi-stage Docker build, CI matrix test runner, Terraform IaC |

---

## Universal Evaluation Workflow

Every evaluation project contains its own `EVAL_BENCHMARK.md`:

```powershell
# 1. Switch into the project folder:
cd g:\ReplitProjects\skills-eval-lab\<project-name>

# 2. Test Candidate A:
git checkout -b test-candidate-a
# Tell the agent: "Apply skill '<candidate-a>' to complete the benchmark in EVAL_BENCHMARK.md"
git add . && git commit -m "Candidate A implementation"

# 3. Test Candidate B:
git checkout main
git checkout -b test-candidate-b
# Tell the agent: "Apply skill '<candidate-b>' to complete the benchmark in EVAL_BENCHMARK.md"
git add . && git commit -m "Candidate B implementation"

# 4. Compare outputs:
git diff test-candidate-a..test-candidate-b --stat
```
