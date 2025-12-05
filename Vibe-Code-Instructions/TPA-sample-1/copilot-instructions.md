---
applyTo: "**"
---

# 🧭 Global GitHub Copilot Instructions

## 🧩 Project Overview
This repository contains two main parts:
- **Frontend:** `frontend-next/` — built with Next.js App Router, React (TypeScript), and Tailwind CSS.
- **Backend:** `backend/` — built with .NET Web API (C#).

Copilot must follow the shared rules below across all code, plans, and documentation.

---

## 🗂️ Workflow Rules

### 1. Always Plan Before Implementing
- Before generating or modifying code, **create a plan markdown file** in the relevant folder:
  - `frontend-next/plan/` for frontend work
  - `backend/plan/` for backend work
- the plan must be in a subfolder named after the feature or refactor (e.g., `authentication-plan.md`).
- if the plan is a bugfiix, it must be in the bugs subfolder of plan (e.g., `bugs/login-error/fix-login-error-plan.md`).
- if the plan is a new feature, it must be in the features subfolder of plan (e.g., `features/restaurants-read/restaurants-read-plan.md`).
- The plan must:
  - Explain what will be built or changed and why.
  - Outline technical and architectural steps.
  - Include a **checklist** at the end for implementation verification.
- **Wait for user approval** before generating any code.

### 2. Always Review and Document
- Before planning, **read the corresponding `docs/` folder** to understand the current system.
- After completing an approved plan:
  1. Verify all checklist items are completed.
  2. Document changes or new features in the relevant `docs/` folder.

### 3. Ask, Don’t Assume
If project details, scope, or expectations are unclear, ask clarifying questions instead of making assumptions.

---

## 💡 Architectural & Code Quality Principles

### Simplicity & Readability
- Code must be **clear, explicit, and consistent**.
- Use meaningful names, small focused functions, and self-documenting structures.
- Favor readability and maintainability over optimization or cleverness.

### Separation of Concerns
- UI, business logic, and data access must remain isolated in their respective layers.
- Avoid cross-layer dependencies or tight coupling.

### No Over-Engineering
- Avoid premature abstraction or complex patterns unless justified by duplication or real need.
- Build only what’s necessary for the current scope.

### Testing & Reliability
- do not create tests

### Security & Robustness
- Validate all external inputs.
- Handle errors explicitly and return meaningful, secure responses.
- Never expose internal details, credentials, or stack traces.

---

## 🧱 Folder Conventions
frontend-next/ → Next.js App Router + Tailwind (UI)
backend/ → .NET Web API (Business logic & data access)
plan/ → Feature or refactor plans awaiting approval
docs/ → Documentation of implemented and approved features

---

## 🔗 Domain-Specific Rules
Each main area has its own scoped instruction file:
- `frontend-next.instructions.md` for frontend conventions
- `backend.instructions.md` for backend conventions

Copilot should automatically apply the relevant scoped file when editing inside those folders.