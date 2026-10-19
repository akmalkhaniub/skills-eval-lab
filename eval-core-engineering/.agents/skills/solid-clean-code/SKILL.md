---
name: solid-clean-code
description: Enforces SOLID design principles, Clean Architecture patterns, low cognitive complexity, and Test-Driven Development (TDD). Use when refactoring code, designing extensible object models, or enforcing senior-level code cleanliness.
---

# SOLID Principles & Clean Code Skill
**Source:** Inspired by [ramziddin/solid-skills](https://github.com/ramziddin/solid-skills)

## The 5 SOLID Directives
1. **Single Responsibility (SRP)**:
   - Each module/class must have only one reason to change. Separate business logic from I/O, formatting, and persistence.
2. **Open/Closed (OCP)**:
   - Classes should be open for extension, but closed for modification. Use strategy interfaces and polymorphism instead of sprawling `if/else` or `switch` statements.
3. **Liskov Substitution (LSP)**:
   - Subtypes must be substitutable for their base types without breaking caller expectations. Never throw `NotImplementedException` in a subclass.
4. **Interface Segregation (ISP)**:
   - Clients should not be forced to depend on methods they do not use. Prefer small, focused interfaces (`Reader`, `Writer`) over monolithic "god" interfaces.
5. **Dependency Inversion (DIP)**:
   - High-level modules must not depend on low-level modules; both should depend on abstractions (interfaces). Inject dependencies via constructors.

## Clean Code Rules
- Functions must be small (< 25 lines) and do one thing well.
- Avoid side effects in query functions (Command-Query Separation).
- Zero magic numbers/strings; extract meaningful named constants.
