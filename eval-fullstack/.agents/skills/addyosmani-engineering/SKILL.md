---
name: addyosmani-engineering
description: Production-grade software engineering discipline covering definition, rigorous planning, modular implementation, verification testing, code review, and deployment checklist. Use when building enterprise-grade features with end-to-end quality gates.
---

# Production Engineering Skill (Addy Osmani Edition)
**Source:** Inspired by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)

## The 6-Stage Execution Pipeline
1. **Define**:
   - Write clear acceptance criteria before modifying code.
   - Clarify edge cases (null inputs, network timeouts, duplicate submissions).
2. **Plan**:
   - Produce a concise architectural implementation step list with affected files.
   - Identify potential regressions and breaking changes in advance.
3. **Build**:
   - Small, cohesive functions (< 30 lines).
   - Defensive programming: validate preconditions and postconditions.
4. **Verify**:
   - Write automated unit tests for every new branch or logic condition.
   - Run linter and type-checker before considering any step complete.
5. **Review**:
   - Self-review code diff against security (OWASP), performance (N+1 queries), and readability.
6. **Ship**:
   - Ensure migrations are backward-compatible and rollback plans exist.
