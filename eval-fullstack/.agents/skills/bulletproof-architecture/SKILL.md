---
name: bulletproof-architecture
description: Feature-based scalable fullstack architecture based on the Bulletproof principles. Enforces domain boundaries, co-located features (api, components, hooks, types), and clean module exports. Use when structuring large-scale web applications.
---

# Bulletproof Architecture Skill
**Source:** Inspired by [alan2207/bulletproof-react](https://github.com/alan2207/bulletproof-react)

## Core Directives
1. **Feature-First Directory Layout**:
   - Organize code by business domain (`features/<feature-name>/`), not technical roles:
     - `features/auth/`
     - `features/billing/`
     - `features/projects/`
   - Each feature encapsulates its own `api/`, `components/`, `hooks/`, `types/`, and `index.ts`.
2. **Strict Module Boundaries**:
   - Other features may only import from `features/<name>/index.ts` (public API).
   - Internal implementation details must remain private to that feature directory.
3. **Shared Kernel**:
   - Code shared across 2+ features resides in `src/components/`, `src/hooks/`, or `src/utils/`.
   - Never import upwards from shared components into specific feature domains.
