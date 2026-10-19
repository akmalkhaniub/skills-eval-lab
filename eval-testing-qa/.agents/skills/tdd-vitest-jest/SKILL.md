---
name: tdd-vitest-jest
description: Test-Driven Development (TDD) and unit/integration testing skill using Vitest and Jest. Enforces the Red-Green-Refactor cycle, test doubles/mocks, deterministic fixtures, and high branch coverage. Use when writing tests or practicing TDD.
---

# Test-Driven Development & Unit Testing Skill

## Core Directives
1. **Red-Green-Refactor Discipline**:
   - Write a failing test first that specifies expected behavior.
   - Write the minimal implementation code necessary to pass the test.
   - Refactor for cleanliness and performance while keeping tests green.
2. **Deterministic Test Isolation**:
   - Tests must never depend on execution order or shared mutable global state.
   - Clean up state in `beforeEach` / `afterEach` hooks.
   - Mock external networks, third-party APIs, and system clocks using `vi.useFakeTimers()` or MSW (Mock Service Worker).
3. **Behavior Over Implementation**:
   - Test user-visible outcomes and public interfaces, not private internals or implementation details.
   - Test edge conditions: empty arrays, boundary values (0, -1, MAX_INT), nulls, and error rejections.
