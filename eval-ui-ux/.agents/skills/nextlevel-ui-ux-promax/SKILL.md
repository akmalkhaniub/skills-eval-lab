---
name: nextlevel-ui-ux-promax
description: High-fidelity visual UX intelligence, layout heuristics, micro-interactions, responsive constraints, and visual hierarchy design. Use when building expressive, modern web interfaces with rich micro-interactions and polish.
---

# UI/UX Pro Max Skill (NextLevel Edition)
**Source:** Inspired by [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

## Core Directives
1. **Visual Hierarchy & Heuristics**:
   - Establish clear F-pattern / Z-pattern eye tracking paths.
   - Primary action must stand out using prominent contrast and depth (elevated shadow or backdrop blur).
   - Secondary actions must be ghost or subtle outline variants.
2. **Micro-Interactions & Animation**:
   - Subtle hover, active, and focus transitions (150ms-250ms `cubic-bezier(0.4, 0, 0.2, 1)`).
   - Interactive feedback: button click ripple/press depth (`active:scale-[0.98]`).
   - Smooth skeleton pulse transitions for async content loading.
3. **Responsive Constraints**:
   - Mobile-first breakpoints: default -> `sm:` -> `md:` -> `lg:` -> `xl:`.
   - Prevent content clipping: fluid typography via `clamp()` or Tailwind utility clamps.
   - Touch targets >= 44x44px on mobile devices.
