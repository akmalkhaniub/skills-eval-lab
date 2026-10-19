---
name: minimax-fullstack-dev
description: Fullstack engineering architecture skill handling API contract definitions, layered backend services, typed database access, error hierarchies, and frontend-backend glue. Use when implementing end-to-end fullstack features.
---

# Fullstack Development Skill (MiniMax Edition)
**Source:** Inspired by [MiniMax-AI/skills](https://github.com/MiniMax-AI/skills)

## Core Directives
1. **API Contracts & Type Sharing**:
   - Define shared schemas using Zod, TypeBox, or tRPC before writing route handlers.
   - Separate request validation, response serialization, and business logic.
   - Strict typing across the boundary: frontend client types must directly derive from API schemas.
2. **Service & Data Layer Separation**:
   - Controller / Route Handler -> Service Layer -> Repository / ORM Layer.
   - Controllers only parse requests, invoke services, and return standard HTTP envelopes `{ data, error, meta }`.
   - Never leak raw ORM errors or database models directly to the HTTP response.
3. **Error Hierarchy**:
   - Use custom error classes: `NotFoundError`, `UnauthorizedError`, `ConflictError`, `ValidationError`.
   - Centralized error-handling middleware that maps domain errors to standard HTTP status codes.
