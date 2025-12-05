---
applyTo: "frontend-next/**"
---

# 🎨 Frontend Instructions — Next.js + Tailwind

> ⚠️ Always follow the global workflow defined in `.github/copilot-instructions.md`  
> before planning or implementing any change.

---

## 🧱 Stack & Structure
- Framework: **Next.js (App Router)** with **React + TypeScript**
- Styling: **Tailwind CSS**
- Key folders:
  - `components/` → UI components only
  - `hooks/` → state management or data fetching logic
  - `services/` → backend API or external data integrations
  - `plan/` and `docs/` → planning and documentation (per global workflow)
- Prefer **server components** by default; use **client components** only when interactivity is required.

---

## ⚙️ Coding Conventions
- **Separation of concerns:**  
  - Never fetch data or handle business logic directly in UI components.  
  - Move data access to `hooks` or `services`.
- **Type safety:** All files and props must be strongly typed.
- **Imports:** Follow existing import patterns and grouping conventions.
- **Prettier/ESLint:** Always auto-format code; never disable linting rules without justification.
- **Comments:** Explain *why* something is done, not *what* it does.

---

## 🎨 Styling Rules
- Use **Tailwind CSS** utility classes; avoid external CSS unless necessary.
- Keep class lists short and readable — extract long or repeated patterns into reusable components or helper classes.
- Maintain visual consistency by reusing design tokens (colors, spacing, etc.).
- Ensure **responsive design** and **accessibility (ARIA, semantic HTML)**.

---

## 🧠 Code Style & Quality
- Keep components small and focused on a single responsibility.
- Use meaningful, descriptive names for variables and functions.
- Avoid premature abstraction — refactor only when duplication or complexity warrants it.
- Always include **error**, **loading**, and **empty** states for async or data-driven components.
- Write self-documenting code — prefer clarity over brevity.

---

## 🧪 Testing
- Use **React Testing Library** for component testing.
- Use **MSW (Mock Service Worker)** for API mocking in tests.
- Every custom hook or service with business logic should have tests.
- Test for multiple states: *loading*, *success*, *error*, and *empty*.

---

## 🚀 Performance & Accessibility
- Use **lazy loading** and **code splitting** when appropriate.
- Apply `React.Suspense` and `ErrorBoundary` for robust async data handling.
- Verify semantic structure and accessibility compliance before merge.

---

## ✅ Summary
- Follow the **global workflow**: `plan → approve → implement → document`.
- Maintain **separation of concerns** (UI, logic, data).
- Prioritize **readability**, **simplicity**, and **type safety**.
- Write **tested**, **accessible**, and **maintainable** code.

---

### 💡 Tip
When in doubt, **prefer convention over invention** — align new code with existing project patterns.
