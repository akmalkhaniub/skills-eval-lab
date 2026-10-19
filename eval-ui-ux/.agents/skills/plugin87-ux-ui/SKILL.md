---
name: plugin87-ux-ui
description: Design-system-first UI/UX engineering with strict DTCG design tokens, WCAG 2.2 AAA accessibility rules, and multi-theme tokens. Use when building production-grade components requiring standardized design tokens and accessibility compliance.
---

# UI/UX Engineering Skill (Plugin87 Edition)
**Source:** Inspired by [plugin87/ux-ui-agent-skills](https://github.com/plugin87/ux-ui-agent-skills)

## Core Directives
1. **Design Tokens First (DTCG Standard)**:
   - Never hardcode raw hex, rgb, or rem units directly into components.
   - Use semantic design tokens:
     - Surface: `var(--color-surface-primary)`, `var(--color-surface-elevated)`
     - Text: `var(--color-text-primary)`, `var(--color-text-muted)`
     - Border: `var(--color-border-subtle)`, `var(--color-border-focus)`
     - Radius & Spacing: `var(--radius-md)`, `var(--space-4)`
2. **Accessibility (WCAG 2.2 AA / AAA)**:
   - Mandatory contrast ratio >= 4.5:1 for body text, >= 3:1 for large text and UI components.
   - Full keyboard navigability: Tab, Enter, Space, Escape, and arrow keys where applicable.
   - Visible and high-contrast focus rings (`outline: 2px solid var(--color-focus-ring)`).
   - Correct ARIA attributes: `aria-expanded`, `aria-controls`, `aria-live`, `aria-describedby`.
3. **Component Architecture**:
   - Decompose into composite atoms/molecules.
   - Support controlled and uncontrolled states.
   - Include distinct loading skeletons, empty states, and error boundaries.
