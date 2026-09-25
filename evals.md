---
name: evals
description: Audits generated code and specs against a 10-point pass/fail checklist before finishing a task.
---

# Quality Evals Skill

When invoked, audit the latest code changes, UI components, or spec files against this checklist:
1. **Pass/Fail Check:** Does the output match the acceptance criteria in `spec.html`?
2. **Design Drift:** Are any non-standard UI components or hardcoded hex colors used?
3. **Edge Case Check:** Are loading states, empty states, and error handling implemented?
4. **Clean Code:** Are there unused imports, placeholder data, or inline styles?

Output a structured score (e.g., 9/10 Pass) and list explicit fix instructions for any failed checks.