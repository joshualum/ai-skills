---
name: sync
description: Updates spec.html and design.md to match real-time code and architectural changes.
---

# Spec Synchronization Skill

Whenever code changes alter the database schema, UI components, or feature scope:
1. Scan the modified files in `/src`.
2. Update the corresponding tables in `spec.html` (PRD, Design, or Tech tab).
3. Confirm all documentation reflects the ground truth of the production build.