# Database & Systems Performance Benchmark

This evaluation project compares three database and performance engineering skills:
1. **`db-schema-migrations`**: Zero-downtime expand-contract schema evolution and non-blocking index additions.
2. **`query-optimization-indexing`**: SQL optimization, composite/partial indexing, and N+1 prevention.
3. **`cache-redis-patterns`**: Cache-aside, distributed lock stampede protection, and key hygiene.

---

## Benchmark Challenge: High-Throughput Activity Feed & Notification Store

### The Test Prompt
> "Design and implement a scalable **User Activity Feed & Event Stream** in TypeScript + PostgreSQL + Redis:
> 1. Schema & Migration: Design tables for `activities` (id, user_id, actor_id, verb, metadata, created_at, read_at). Write a migration script that safely adds a multi-tenant `organization_id` column to an existing 10M row table without downtime or table lock.
> 2. Query Optimization: Write the query to fetch the latest 20 unread activities for user X with actor profile data. Add appropriate composite indexes and demonstrate elimination of N+1 queries.
> 3. Caching Layer: Implement a Redis caching layer using Cache-Aside with jittered TTL and mutex locks to prevent cache stampedes on viral events."

---

## How to Run the Evaluation

1. **Test Candidate A (`db-schema-migrations`)**:
   ```powershell
   git checkout -b test-db-migrations
   # Prompt: "Apply the 'db-schema-migrations' skill to implement the solution described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: DB migrations implementation"
   ```

2. **Test Candidate B (`query-optimization-indexing`)**:
   ```powershell
   git checkout main
   git checkout -b test-query-opt
   # Prompt: "Apply the 'query-optimization-indexing' skill to implement the solution described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: Query optimization implementation"
   ```

3. **Test Candidate C (`cache-redis-patterns`)**:
   ```powershell
   git checkout main
   git checkout -b test-redis-cache
   # Prompt: "Apply the 'cache-redis-patterns' skill to implement the solution described in EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: Redis caching implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (Migrations) | Candidate B (Query Opt) | Candidate C (Redis Cache) |
| :--- | :--- | :--- | :--- |
| **Zero-Downtime Migration Safety** | | | |
| **Index Design & Query Efficiency** | | | |
| **N+1 Query Elimination** | | | |
| **Cache Invalidation & Stampede Defense** | | | |
| **Memory / Connection Pool Hygiene** | | | |
