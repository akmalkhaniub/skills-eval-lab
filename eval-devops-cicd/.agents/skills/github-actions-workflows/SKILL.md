---
name: github-actions-workflows
description: GitHub Actions workflow engineering skill. Focuses on matrix builds, aggressive caching (actions/cache), minimal permission scopes (GITHUB_TOKEN permissions: read-all), secret masking, and deployment environments with required reviewers. Use when creating CI/CD workflows.
---

# GitHub Actions CI/CD Workflows Skill

## Core Directives
1. **Least-Privilege Token Permissions**:
   - Explicitly declare top-level `permissions:` block in all workflows:
     ```yaml
     permissions:
       contents: read
       pull-requests: write
     ```
   - Never rely on default broad write permissions.
2. **Speed & Caching Optimization**:
   - Cache package manager dependencies (`actions/setup-node` with `cache: 'npm'`).
   - Use concurrency groups (`concurrency: { group: ..., cancel-in-progress: true }`) to cancel redundant in-flight builds on push.
3. **Branch Protection & Deployment Gates**:
   - Deployments must reference explicit GitHub Environments with protection rules and approvals.
   - Run linter, type-check, and unit tests in parallel matrix jobs before triggering deployment stages.
