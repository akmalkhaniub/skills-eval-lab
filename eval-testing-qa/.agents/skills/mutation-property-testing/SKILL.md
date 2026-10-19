---
name: mutation-property-testing
description: Advanced testing skill for property-based fuzzing and mutation testing. Uses tools like Fast-Check and Stryker to uncover hidden edge cases, verify invariants, and test the resilience of your test suite. Use when creating bulletproof test suites.
---

# Property-Based & Mutation Testing Skill

## Core Directives
1. **Property-Based Invariants**:
   - Instead of writing single example inputs, test universal invariants across thousands of randomized inputs (using Fast-Check).
   - Invariant examples:
     - Serialization: `deserialize(serialize(x)) === x` (round-trip equality)
     - Idempotency: `fn(fn(x)) === fn(x)`
     - Ordering: sorting an array never changes length or removes items
2. **Mutation Testing (Stryker)**:
   - Verify that tests actually fail when bugs are injected into the code (mutants killed vs survived).
   - Require a mutation score threshold >= 80% on critical business logic.
