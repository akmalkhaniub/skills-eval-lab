# DevOps & CI/CD Pipeline Skills Benchmark

This evaluation project compares three DevOps and infrastructure automation skills:
1. **`docker-container-hardening`**: Multi-stage builds, non-root user execution, and distroless minimal base images.
2. **`github-actions-workflows`**: Least-privilege GITHUB_TOKEN permissions, dependency caching, and matrix test jobs.
3. **`terraform-iac-platform`**: Remote state locking, modular structure, and input variable validation.

---

## Benchmark Challenge: Production Cloud Containerization & Deployment Pipeline

### The Test Prompt
> "Build the containerization and CI/CD infrastructure for a production full-stack web service:
> 1. Hardened Dockerfile: Create a multi-stage Dockerfile for a Node.js/TypeScript or Go app that:
>    - Builds the production bundle in a separate builder stage.
>    - Uses a non-root user and minimal runtime base image (Alpine or Distroless).
>    - Includes a proper `.dockerignore` to block local node_modules, .env, and .git.
> 2. GitHub Actions CI/CD: Write `.github/workflows/ci.yml` that:
>    - Sets minimal permissions (`contents: read`).
>    - Runs linting, type-checking, and tests in parallel using matrix caching.
>    - Builds and scans the Docker image for CVEs using Trivy before deploying."

---

## How to Run the Evaluation

1. **Test Candidate A (`docker-container-hardening`)**:
   ```powershell
   git checkout -b test-docker-hardening
   # Prompt: "Apply the 'docker-container-hardening' skill to write the container configuration described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: Docker hardening implementation"
   ```

2. **Test Candidate B (`github-actions-workflows`)**:
   ```powershell
   git checkout main
   git checkout -b test-github-actions
   # Prompt: "Apply the 'github-actions-workflows' skill to write the CI/CD pipeline described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: GitHub Actions implementation"
   ```

3. **Test Candidate C (`terraform-iac-platform`)**:
   ```powershell
   git checkout main
   git checkout -b test-terraform
   # Prompt: "Apply the 'terraform-iac-platform' skill to provision the cloud infrastructure described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: Terraform implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (Docker) | Candidate B (GitHub Actions) | Candidate C (Terraform) |
| :--- | :--- | :--- | :--- |
| **Security Hardening (Non-root / Least Privilege)** | | | |
| **Build & Cache Efficiency** | | | |
| **Vulnerability Scanning & Safety Gates** | | | |
| **Maintainability & Modularity** | | | |
| **Reproducibility Across Environments** | | | |
