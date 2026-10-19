---
name: playwright-e2e
description: End-to-end (E2E) browser testing and visual regression testing using Playwright. Focuses on user-centric locators, resilient wait strategies, Page Object Models (POM), accessibility checks, and cross-browser execution. Use when creating browser tests.
---

# Playwright E2E Testing Skill

## Core Directives
1. **User-Centric Locators**:
   - Prefer role-based and label-based locators: `page.getByRole('button', { name: 'Submit' })`, `page.getByLabel('Email')`.
   - Never use brittle CSS selectors (`div > div.css-123xyz > span`) or arbitrary XPath.
2. **Auto-Waiting & Zero Flakiness**:
   - Leverage Playwright's built-in auto-waiting for actionability (visible, enabled, stable).
   - Never use arbitrary `page.waitForTimeout(3000)`. Wait on explicit network responses or DOM states.
3. **Page Object Model (POM)**:
   - Encapsulate page UI structures into clean Page Objects (`LoginPage`, `CheckoutPage`).
   - Keep test files focused on business user journeys rather than low-level DOM queries.
4. **Automated Accessibility Assertion**:
   - Integrate `@axe-core/playwright` to run automated accessibility scans on key page states.
