---
name: db-schema-migrations
description: Database schema evolution and zero-downtime migration skill. Follows the expand-contract pattern, safe column additions/drops, backward-compatible migrations with Prisma, Drizzle, and Flyway. Use when creating or modifying database schemas.
---

# Zero-Downtime Database Schema Migration Skill

## Core Directives
1. **The Expand-Contract Pattern**:
   - Step 1 (Expand): Add new column or table as nullable or with safe default. Both old and new code work simultaneously.
   - Step 2 (Dual Write / Backfill): Populate data asynchronously in batches without table locks.
   - Step 3 (Contract): Switch application code to read from new structure, then safely drop obsolete fields in a subsequent deployment.
2. **Never Block Production Tables**:
   - In PostgreSQL / MySQL: Avoid full-table locks.
   - Create indexes concurrently (`CREATE INDEX CONCURRENTLY`).
   - Do not add `NOT NULL` constraints on existing large tables without a default value or check constraint.
3. **Rollback Safety**:
   - Every migration must have an idempotent rollback or down-migration procedure.
