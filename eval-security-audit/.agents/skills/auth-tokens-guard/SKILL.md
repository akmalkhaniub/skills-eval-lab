---
name: auth-tokens-guard
description: Production authentication and authorization security skill. Covers JWT lifecycle, refresh token rotation, secure cookie flags (HttpOnly, SameSite, Secure), session management, and RBAC/ABAC enforcement. Use when building or auditing authentication systems.
---

# Authentication & Token Security Skill

## Core Directives
1. **JWT & Session Security**:
   - Short expiration times for access tokens (e.g., 5-15 minutes).
   - Use rotating refresh tokens with family tracking to detect and revoke compromised token chains.
   - Store sensitive auth tokens in `HttpOnly`, `Secure`, `SameSite=Strict` cookies to block JavaScript theft via XSS.
2. **Password & Hashing Standards**:
   - Passwords must be hashed using Argon2id or bcrypt (work factor >= 12).
   - Never roll custom cryptographic primitives or hashing algorithms.
3. **Role-Based Access Control (RBAC) Enforcement**:
   - Centralize authorization logic into reusable guards/middleware (`requireRole('admin')`, `can('read', 'invoice')`).
   - Audit trail: log all failed authentication attempts and privilege escalations with client IP and user agent.
