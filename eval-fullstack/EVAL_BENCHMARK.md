# Fullstack Skills Evaluation Benchmark

This evaluation project compares three full-stack software engineering skills:
1. **`minimax-fullstack-dev`**: Focuses on API contracts, layered architecture (Controller -> Service -> Repo), and typed error handling.
2. **`addyosmani-engineering`**: Focuses on the 6-stage engineering lifecycle (Define, Plan, Build, Verify, Review, Ship).
3. **`bulletproof-architecture`**: Focuses on feature-first co-location, strict module boundaries, and clean imports.

---

## Benchmark Challenge: SaaS Workspace Billing & Feature Gate

### The Test Prompt
> "Build a complete **Workspace Billing & Feature Gate** module in TypeScript:
> 1. Data Schema: `Workspace`, `SubscriptionPlan` (Free, Pro, Enterprise), and `FeatureGate` (e.g., max_members, api_access).
> 2. Backend Service: `BillingService` with methods `upgradePlan(workspaceId, newPlanId)` and `checkFeatureAccess(workspaceId, featureKey)`. Must enforce validation, transactions, and domain error hierarchy.
> 3. API Route Handler: Clean REST or tRPC endpoint with input validation via Zod, error handling envelope, and authentication guard.
> 4. Frontend Client Hook / Component: `useFeatureGate(featureKey)` React hook and an upgrade prompt modal when access is denied."

---

## How to Run the Evaluation

1. **Test Candidate A (`minimax-fullstack-dev`)**:
   ```
   git checkout -b test-minimax
   # Prompt: "Apply the 'minimax-fullstack-dev' skill to complete the task defined in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: minimax implementation"
   ```

2. **Test Candidate B (`addyosmani-engineering`)**:
   ```
   git checkout main
   git checkout -b test-addyosmani
   # Prompt: "Apply the 'addyosmani-engineering' skill to complete the task defined in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: addyosmani implementation"
   ```

3. **Test Candidate C (`bulletproof-architecture`)**:
   ```
   git checkout main
   git checkout -b test-bulletproof
   # Prompt: "Apply the 'bulletproof-architecture' skill to complete the task defined in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: bulletproof implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (MiniMax) | Candidate B (Addy Osmani) | Candidate C (Bulletproof) |
| :--- | :--- | :--- | :--- |
| **Separation of Concerns** (Controller / Service / Data) | | | |
| **Type Safety & Schema Validation** (Zod / TypeScript derivation) | | | |
| **Error Handling Envelope & Status Codes** | | | |
| **Folder Architecture & Boundary Hygiene** | | | |
| **Verification & Tests Provided** | | | |
