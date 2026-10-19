# Testing & QA Skills Benchmark

This evaluation project compares three automated testing methodologies:
1. **`tdd-vitest-jest`**: Red-Green-Refactor, test doubles, deterministic isolation, and unit coverage.
2. **`playwright-e2e`**: Resilient browser automation, Page Object Model, network mocking, and a11y scans.
3. **`mutation-property-testing`**: Fast-check property invariants and mutation resilience.

---

## Benchmark Challenge: Multi-Tier E-Commerce Checkout Flow

### The Test Prompt
> "Build a comprehensive test suite for an **E-Commerce Checkout & Discount Engine**:
> 1. Domain Logic: A discount calculator applying tiered discounts, coupon codes (e.g. 'SUMMER20'), and tax calculation per region.
> 2. Unit & Integration Tests (Vitest): Test discount limits, negative values, coupon expiration, and order subtotal calculations with 100% branch coverage.
> 3. E2E Browser Test (Playwright): A resilient test simulating a user adding an item to the cart, applying a discount code, filling out the shipping form, and completing checkout. Use Page Object Model and verify accessibility using axe-core."

---

## How to Run the Evaluation

1. **Test Candidate A (`tdd-vitest-jest`)**:
   ```powershell
   git checkout -b test-tdd
   # Prompt: "Apply the 'tdd-vitest-jest' skill to implement the test suite described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: TDD Vitest implementation"
   ```

2. **Test Candidate B (`playwright-e2e`)**:
   ```powershell
   git checkout main
   git checkout -b test-playwright
   # Prompt: "Apply the 'playwright-e2e' skill to implement the test suite described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: Playwright E2E implementation"
   ```

3. **Test Candidate C (`mutation-property-testing`)**:
   ```powershell
   git checkout main
   git checkout -b test-property-testing
   # Prompt: "Apply the 'mutation-property-testing' skill to implement the test suite described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: Property testing implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (TDD) | Candidate B (Playwright) | Candidate C (Property) |
| :--- | :--- | :--- | :--- |
| **Edge Case & Boundary Coverage** | | | |
| **Test Flakiness & Determinism** | | | |
| **Selector Resilience & Page Object Cleanliness** | | | |
| **Mocking & Fixture Hygiene** | | | |
| **Execution Speed & Maintainability** | | | |
