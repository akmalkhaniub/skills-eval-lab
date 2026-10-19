---
name: terraform-iac-platform
description: Terraform and OpenTofu Infrastructure as Code (IaC) engineering skill. Enforces remote backend state locking, modular architecture, variable validation rules, and automated security scanning with tfsec/trivy. Use when writing infrastructure code.
---

# Terraform & OpenTofu IaC Skill

## Core Directives
1. **State & Remote Locking**:
   - Always configure remote state storage (S3 + DynamoDB locking or GCS state bucket).
   - Never commit `.tfstate` or `.tfvars` containing secrets to version control.
2. **Modular Architecture**:
   - Split configurations into reusable modules: `root -> environments/ (prod, staging) -> modules/ (vpc, db, compute)`.
   - Separate state files per environment to reduce blast radius.
3. **Variable Validation & Outputs**:
   - Add explicit `validation` blocks with error messages to all input variables.
   - Mark sensitive outputs (`sensitive = true`) to prevent plaintext leakage in CI logs.
