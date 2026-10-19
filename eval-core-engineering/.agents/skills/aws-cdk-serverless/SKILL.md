---
name: aws-cdk-serverless
description: AWS Cloud architecture skill specializing in AWS CDK, serverless patterns (Lambda, DynamoDB, API Gateway, SQS/SNS), IAM least-privilege policies, and CloudWatch observability. Use when building or deploying on AWS.
---

# AWS CDK & Serverless Architecture Skill
**Source:** Inspired by [aws-samples/sample-aws-solutions-skills](https://github.com/aws-samples/sample-aws-solutions-skills) & community CDK skills

## Core Directives
1. **Infrastructure as Code (CDK Best Practices)**:
   - Organize by Construct trees: App -> Stacks -> Nested Stacks / L3 Constructs.
   - Use strongly typed construct props and environment-agnostic stack definitions.
2. **Serverless Architecture**:
   - Lambda: Single-purpose event handlers; keep package sizes minimal; configure memory and timeout conservatively.
   - DynamoDB: Single-table or targeted multi-table design with explicitly defined partition/sort keys.
   - Event-Driven: Decouple services with SQS queues and SNS topics with Dead Letter Queues (DLQ).
3. **IAM Least Privilege**:
   - Never grant `*` permissions or attach full admin managed policies.
   - Restrict actions to specific resource ARNs (`s3:GetObject` on `arn:aws:s3:::bucket/*`).
   - Store API keys and database credentials in AWS Secrets Manager or SSM Parameter Store.
