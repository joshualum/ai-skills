# ai-skills
dedicated repository of skills just for building SaaS products smartly

# AI-Native Product Development Workflow

This workflow adapts Peter Yang's AI-native SaaS building process to leverage custom skills (`spec.md`, `design-md.md`, `evals.md`, `anti-slop.md`, `sync.md`) alongside zero-cost or generous-tier AI tools like OpenAI Codex (CLI/ChatGPT Free), Cursor Free, or v0.dev.

---

## Workflow Overview

Phase 1: Problem Discovery (ChatGPT / Codex CLI)
Phase 2: Visual Identity (ChatGPT + design-md)
Phase 3: Screen Prototyping (v0.dev / Codex Web)
Phase 4: HTML Spec (spec.md Synthesis)
Phase 5: Complete Screens (v0.dev / Codex UI)
Phase 6: Build & Test (Codex CLI / Cursor / Evals)

---

## Phase 1: Problem Discovery & Validation
**Goal:** Define the user problem, target audience, and business feasibility before writing any code or drawing mockups.

* **Tool:** ChatGPT Free / OpenAI Codex CLI / Claude Free Chat
* **Skill Used:** `/spec` (Execution Mode: Phase 1)

### Steps:
1. Open your AI chat tool and run your `/spec` skill in **Phase 1 Mode**.
2. Provide your rough idea:
   > *"I want to build [SaaS Idea]. Let's run Phase 1 of /spec to define the user problem, ICP, market evidence, and core features."*
3. Answer any clarifying questions asked by the AI agent.
4. Finalize the initial problem definition, target persona, success metrics, and V1 scope.

---

## Phase 2: Visual Direction & Design Tokens
**Goal:** Establish the app's visual identity, typography, spacing, and color tokens so the AI doesn't generate generic UI "slop".

* **Tool:** ChatGPT Free / Claude Free Chat
* **Skill Used:** `/design-md` + Optional screenshots for inspiration

### Steps:
1. Find a reference design or website you like (e.g., Mobbin, Dribbble, or existing SaaS platforms).
2. Upload 1–3 screenshots to your AI chat tool and invoke `/design-md`:
   > *"Analyze these screenshots and generate a `design.md` file for [Product Name]. Include visual principles, CSS color tokens, typography rules, and spacing."*
3. Save the generated output locally as `design.md` in your project folder.

---

## Phase 3: Prototype Key Screens
**Goal:** Generate 2 core screen mockups (e.g., main dashboard and public landing page) to visualize the product layout before writing specs.

* **Tool:** v0.dev (Free Tier), Codex Web, or OpenCode / Cursor Free
* **Input Files:** `design.md`

### Steps:
1. Open **v0.dev** or **Codex** (UI generation interface).
2. Attach `design.md` and prompt:
   > *"Create two key screens for [Product Name]: (1) Landing Page, (2) Main Dashboard. Use the color tokens and typography in design.md. Provide 2 layout variations."*
3. Apply taste and give specific feedback to refine the mockups.
4. Export the resulting mockups as HTML or a `.zip` file into your project workspace.

---

## Phase 4: Generate Consolidated Interactive Spec
**Goal:** Merge the Phase 1 problem definition, `design.md`, and exported screen mockups into a single interactive, tabbed `spec.html` document.

* **Tool:** ChatGPT Free / OpenAI Codex CLI / Claude Free
* **Skill Used:** `/spec` (Execution Mode: Phase 2) + `/anti-slop`

### Steps:
1. In your AI terminal or chat, attach your Phase 1 output, `design.md`, and mockup files.
2. Run your `/spec` skill in **Phase 2 Mode**:
   > *"Combine these inputs into a single tabbed `spec.html` file containing: Tab 1 (PRD), Tab 2 (Design System & Component Library), Tab 3 (Tech Spec & DB Schema). Run /anti-slop to keep text direct."*
3. Save the generated raw HTML code as `spec.html` (or `plan.html`) in your project root.
4. Open `spec.html` in your browser to verify that all 3 tabs look clean and accurate.

---

## Phase 5: Design Full Screen Suite & States
**Goal:** Generate mockups for all supporting views, empty states, error states, and onboarding flows.

* **Tool:** v0.dev (Free Tier), Codex Web, or Cursor
* **Input Files:** `spec.html`

### Steps:
1. Upload `spec.html` to your UI tool.
2. Prompt:
   > *"Review spec.html and generate mockups for all remaining screens, including empty states, onboarding, and mobile responsive views."*
3. Review and export all generated screens as `design.html` (or a `.zip` archive).

---

## Phase 6: Build, Evaluate, & Sync
**Goal:** Build the application using your AI coding assistant while keeping documentation and code in sync.

* **Tool:** OpenAI Codex CLI (Free on ChatGPT tier), Cursor Free, or OpenCode / Aider
* **Skills Used:** `/evals` + `/sync`

### Steps:
1. Open your terminal or IDE in your project root containing `spec.html`, `design.md`, and your exported screens.
2. Provide your AI coding tool with initial instructions:
   > *"Review spec.html and design.md. Ask any clarifying questions or list ambiguities before you start building."*
3. Let the agent build the app incrementally (database setup, API endpoints, core UI pages).
4. Run your `/evals` skill to perform quality control:
   > *"Run /evals on the recent codebase changes. Audit against spec requirements, design drift, empty states, and clean code."*
5. Fix any flagged issues, then update your documentation using `/sync`:
   > *"Run /sync to update spec.html so that the database schema and component library match our latest codebase."*

---

## Summary of Core Skills

| Skill | Description | Usage Command |
| :--- | :--- | :--- |
| **`spec.md`** | Problem discovery & generation of interactive `spec.html` | `/spec` |
| **`design-md.md`** | Creates CSS tokens, layout rules, and UI system | `/design-md` |
| **`anti-slop.md`** | Eliminates marketing fluff and enforces direct copy | `/anti-slop` |
| **`evals.md`** | Audits codebase against a 10-point pass/fail quality checklist | `/evals` |
| **`sync.md`** | Keeps `spec.html` and `design.md` up-to-date as code changes | `/sync` |
