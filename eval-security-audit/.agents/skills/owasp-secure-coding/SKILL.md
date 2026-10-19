---
name: owasp-secure-coding
description: Hardens applications against OWASP Top 10 vulnerabilities. Enforces strict input validation, parameterized queries, CSRF tokens, secure CORS, and content security policies (CSP). Use when reviewing, auditing, or writing secure code.
---

# OWASP Secure Coding Skill
**Source:** Derived from OWASP Application Security Verification Standard (ASVS)

## Core Directives
1. **Injection Prevention (SQL, NoSQL, OS Command)**:
   - Always use parameterized queries or type-safe ORM prepared statements.
   - Never concatenate raw user input into SQL queries or shell execution strings (`exec`, `spawn`).
2. **Broken Access Control (IDOR & Privilege Escalation)**:
   - Validate ownership on every resource request: check `resource.ownerId === currentUser.id` or verify role permissions before mutating state.
   - Never trust client-supplied user IDs, roles, or organization scopes from request bodies.
3. **Cross-Site Scripting (XSS) & Content Security**:
   - Sanitize HTML inputs using DOMPurify or sanitize-html before rendering.
   - Configure strict Content Security Policy (CSP), `X-Frame-Options: DENY`, and `X-Content-Type-Options: nosniff`.
4. **Data Protection & Secret Hygiene**:
   - Never commit API keys, private keys, or credentials to source control.
   - Use constant-time string comparisons (`crypto.timingSafeEqual`) for HMAC or token checks to prevent timing attacks.
