---
name: query-optimization-indexing
description: SQL query performance optimization, index design (B-tree, GIN, partial indexes), EXPLAIN ANALYZE interpretation, and N+1 query elimination. Use when diagnosing slow queries or optimizing database throughput.
---

# Query Optimization & Indexing Skill

## Core Directives
1. **Index Selection Heuristics**:
   - Create composite indexes matching query filter order: Equality first, then Range (`WHERE status = 'active' AND created_at > ...`).
   - Use covering indexes (`INCLUDE` clause in Postgres) to allow index-only scans and avoid table heap lookups.
   - Use partial indexes for skewed boolean columns (`WHERE is_processed = false`).
2. **Eliminate N+1 Queries**:
   - In ORMs (Prisma, Drizzle, TypeORM), enforce eager loading (`include` / `with`) or batch loading via DataLoader.
   - Avoid loops that make individual database calls (`for (item of list) db.query(...)`).
3. **Analyze Execution Plans**:
   - Always run `EXPLAIN (ANALYZE, BUFFERS)` on slow queries.
   - Watch out for sequential table scans (Seq Scan), high shared buffer reads, or slow nested loops.
