# Core Engineering, SOLID, and Cloud Skills Benchmark

This evaluation project compares skills that enforce senior-level architecture and cloud infrastructure standards:
1. **`solid-clean-code`**: Strict SOLID principles, interface segregation, dependency injection, and clean code limits.
2. **`aws-cdk-serverless`**: AWS CDK constructs, Lambda/DynamoDB serverless patterns, and IAM least-privilege policies.
3. **`gcp-cloud-architecture`**: GCP Cloud Run stateless microservices, Pub/Sub messaging, and GCP Secret Manager security.

---

## Benchmark Challenge: Multi-Channel Order Notification & Invoicing Engine

### The Test Prompt
> "Build an extensible **Order Notification & Invoicing Service**:
> 1. Domain Architecture (SOLID): Implement an `OrderProcessor` that accepts an order and sends notifications across multiple channels (Email, SMS, Slack, Webhook) and generates a PDF invoice.
>    - Must strictly adhere to Open/Closed Principle (new channels can be added without modifying existing classes).
>    - Must use Dependency Inversion (high-level order logic depends on `INotificationChannel` and `IInvoiceStorage` interfaces, injected at runtime).
> 2. Cloud Infrastructure Provisioning:
>    - Create the Infrastructure-as-Code definition (either AWS CDK Stack with Lambda + EventBridge + DynamoDB, or GCP Terraform/Cloud Run + Pub/Sub).
>    - Enforce least-privilege IAM permissions and zero plaintext secrets."

---

## How to Run the Evaluation

1. **Test Candidate A (`solid-clean-code`)**:
   ```
   git checkout -b test-solid
   # Prompt: "Apply the 'solid-clean-code' skill to design and implement the domain layer for the challenge in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: SOLID clean code implementation"
   ```

2. **Test Candidate B (`aws-cdk-serverless`)**:
   ```
   git checkout main
   git checkout -b test-aws-cdk
   # Prompt: "Apply the 'aws-cdk-serverless' skill to provision the infrastructure for the challenge in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: AWS CDK implementation"
   ```

3. **Test Candidate C (`gcp-cloud-architecture`)**:
   ```
   git checkout main
   git checkout -b test-gcp
   # Prompt: "Apply the 'gcp-cloud-architecture' skill to provision the infrastructure for the challenge in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: GCP architecture implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (SOLID) | Candidate B (AWS CDK) | Candidate C (GCP) |
| :--- | :--- | :--- | :--- |
| **Extensibility (Open/Closed Principle)** | | | |
| **Dependency Injection & Decoupling** | | | |
| **Least-Privilege Cloud Security / IAM** | | | |
| **Event-Driven Resilience (DLQ / Retries)** | | | |
| **Unit Testability / Mocking Simplicity** | | | |
