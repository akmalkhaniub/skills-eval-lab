---
name: jakubkrehel-accessibility
description: Dedicated accessibility auditor and WCAG compliance enforcer. Ensures automated a11y testing, keyboard traps prevention, screen reader clarity, and accessible color schemes. Use when performing deep accessibility audits and fixes.
---

# Accessibility & UI Verification Skill
**Source:** Inspired by [jakubkrehel/skills](https://github.com/jakubkrehel/skills)

## Core Directives
1. **Screen Reader Experience**:
   - Provide explicit `aria-label` or `sr-only` text for icon-only buttons.
   - Use semantic landmarks (`<main>`, `<nav>`, `<aside>`, `<header>`, `<footer>`).
   - Associate form inputs with `<label htmlFor="...">` and `<span id="..." role="alert">`.
2. **Keyboard Navigation & Trap Prevention**:
   - Modal dialogs must trap focus inside while open and return focus to trigger on close.
   - Escape key dismisses open overlays, menus, and modals.
   - Logical tab index: do not use positive `tabindex` (> 0). Use `0` or `-1`.
3. **Contrast & Color Blindness**:
   - Never rely on color alone to convey status (combine color with icons or textual tags).
   - Test color pairings for Deuteranopia, Protanopia, and Tritanopia readability.
