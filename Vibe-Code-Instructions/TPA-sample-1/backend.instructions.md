---
applyTo: "backend/**"
---

# ⚙️ Backend Instructions — .NET Web API

> ⚠️ Follow the general planning and documentation workflow defined in `.github/copilot-instructions.md` before starting any implementation.

---

## 🧩 Architectural Guidelines
- **Controllers**: Thin adapters — delegate all logic to services.
- **Services**: Contain business logic only.
- **Repositories**: Encapsulate data access (EF Core or external APIs).
- **DTOs / ViewModels**: Used for input/output; never expose domain entities.
- **Dependency Injection** for all services and repositories.
- **Async/Await** for all I/O operations.

---

## ⚙️ Coding Rules
- **Validation**: Use FluentValidation or data annotations for request models.
- **Error Handling**: Centralize exception handling; return appropriate HTTP codes.
- **Logging**: Use structured logging (e.g., Serilog).
- **Testing**: Unit tests for services, integration tests for controllers (e.g., with WebApplicationFactory).

---

## 🔒 Security & Stability
- Validate and sanitize all inputs.
- Do not leak stack traces or internal data.
- Handle edge cases and null values explicitly.
- Enforce authentication/authorization where required.

---

## ✅ Summary
- Follow the global workflow and architectural boundaries.
- Maintain separation of concerns and clear layering.
- Keep code simple, consistent, and testable.