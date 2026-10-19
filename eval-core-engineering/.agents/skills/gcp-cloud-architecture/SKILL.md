---
name: gcp-cloud-architecture
description: Google Cloud Platform (GCP) architecture skill covering Cloud Run, Cloud Functions, Pub/Sub, Firestore/Cloud SQL, Secret Manager, and Vertex AI integrations. Use when designing, building, or deploying on Google Cloud.
---

# Google Cloud Platform (GCP) Architecture Skill
**Source:** Inspired by [google/skills](https://github.com/google/skills)

## Core Directives
1. **Containerized Compute (Cloud Run)**:
   - Stateless microservices deployed on Cloud Run with container concurrency and auto-scaling rules.
   - Separate HTTP traffic routing using revisions and traffic-splitting tags.
2. **Data & Messaging**:
   - Asynchronous decoupled processing via Google Cloud Pub/Sub with dead-letter topics.
   - Database persistence using Cloud SQL (with connection pooler / Cloud SQL Auth proxy) or Firestore in Datastore mode.
3. **Security & Identity**:
   - Use dedicated service accounts per workload with narrow IAM roles (e.g. `roles/secretmanager.secretAccessor`).
   - Store environment configurations and keys in GCP Secret Manager, not in Dockerfiles or repo commits.
   - Enable Cloud Logging / Cloud Trace structured logging.
