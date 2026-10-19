---
name: cache-redis-patterns
description: High-performance caching strategies using Redis. Implements Cache-Aside, Write-Through, Stale-While-Revalidate, cache invalidation, key namespaces, and cache stampede prevention using distributed locks. Use when designing high-throughput data caches.
---

# Redis Caching Patterns Skill

## Core Directives
1. **Caching Topologies**:
   - Cache-Aside (Lazy Loading): Read from Redis first; if miss, query primary DB and populate cache with TTL.
   - Write-Through: Write to database and update cache atomically.
2. **Preventing Cache Stampede & Avalanche**:
   - Add jitter to TTLs (`base_ttl + random_jitter`) to prevent massive simultaneous expirations.
   - Use mutex / single-flight locking for expensive computation misses so only one worker queries the database while others wait.
3. **Key Namespacing & Memory Hygiene**:
   - Structured key format: `<env>:<domain>:<entity>:<id>` (e.g., `prod:users:profile:42`).
   - Always configure explicit TTLs; never set keys without expiration unless permanently managed.
   - Use Redis data structures appropriately (Hashes for objects, Sorted Sets for leaderboards/time-series).
