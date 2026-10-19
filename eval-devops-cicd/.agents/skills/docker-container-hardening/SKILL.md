---
name: docker-container-hardening
description: Production Docker containerization and security hardening skill. Enforces multi-stage builds, non-root users, minimal attack surface base images (Distroless / Alpine), layer caching, and vulnerability scanning. Use when authoring or reviewing Dockerfiles.
---

# Docker Container Hardening & Optimization Skill

## Core Directives
1. **Multi-Stage Builds**:
   - Separate build-time dependencies (compilers, npm devDependencies) from runtime images.
   - Final production stage must contain only compiled artifacts and production dependencies.
2. **Non-Root Execution**:
   - Explicitly create and switch to a non-privileged user (`USER node` or `USER appuser`).
   - Never run container processes as root in production.
3. **Minimal Attack Surface**:
   - Use `distroless` or slim/alpine minimal base images to eliminate unnecessary shell utilities and binaries.
   - Use `.dockerignore` to prevent leaking `.git`, `.env`, keys, and node_modules into the build context.
4. **Build Layer Caching & Metadata**:
   - Copy dependency manifests (`package.json`, `package-lock.json`) before application source code to leverage build cache.
   - Pin base images to specific digest SHA or semantic versions rather than floating `:latest`.
