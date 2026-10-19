# UI/UX Skills Evaluation Benchmark

This evaluation project compares three distinct UI/UX skills:
1. **`plugin87-ux-ui`**: Focuses on DTCG design tokens and WCAG 2.2 AAA accessibility.
2. **`nextlevel-ui-ux-promax`**: Focuses on visual hierarchy, heuristics, micro-interactions, and aesthetics.
3. **`jakubkrehel-accessibility`**: Focuses on screen reader fidelity, keyboard trap prevention, and a11y testing.

---

## Benchmark Challenge: Interactive Metric Card & Drilldown

### The Test Prompt
> "Build an interactive, themeable **Analytics Metric Card** in React with TypeScript and Tailwind CSS. The component must display:
> - Metric title, value with trend percentage badge (positive/negative indicator)
> - An interactive mini sparkline chart or bar progression with hover tooltip
> - A kebab action menu with at least 3 actions (Export, Set Alert, Drilldown)
> - A loading skeleton state and an error state with retry button
> - Drilldown modal dialog that opens when clicking 'Drilldown' with focus trap and escape-to-close."

---

## How to Run the Evaluation

1. **Test Candidate A (`plugin87-ux-ui`)**:
   ```
   git checkout -b test-plugin87
   # Prompt the agent:
   "Follow the instructions in the 'plugin87-ux-ui' skill to build the component in src/components/MetricCard.tsx according to EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate A: plugin87 implementation"
   ```

2. **Test Candidate B (`nextlevel-ui-ux-promax`)**:
   ```
   git checkout main
   git checkout -b test-nextlevel
   # Prompt the agent:
   "Follow the instructions in the 'nextlevel-ui-ux-promax' skill to build the component in src/components/MetricCard.tsx according to EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate B: nextlevel implementation"
   ```

3. **Test Candidate C (`jakubkrehel-accessibility`)**:
   ```
   git checkout main
   git checkout -b test-jakubkrehel
   # Prompt the agent:
   "Follow the instructions in the 'jakubkrehel-accessibility' skill to build the component in src/components/MetricCard.tsx according to EVAL_BENCHMARK.md."
   git add . && git commit -m "Candidate C: jakubkrehel implementation"
   ```

---

## Evaluation Scorecard (Score 1-5)

| Metric | Candidate A (Plugin87) | Candidate B (NextLevel) | Candidate C (Jakub) |
| :--- | :--- | :--- | :--- |
| **Token Discipline** (No hardcoded hex/arbitrary values) | | | |
| **Micro-Interactions** (Transitions, hover/active states) | | | |
| **Accessibility** (Keyboard traps, ARIA roles, contrast) | | | |
| **Modularity & Types** (Clean props interface, sub-components) | | | |
| **Empty / Error / Loading States** | | | |
