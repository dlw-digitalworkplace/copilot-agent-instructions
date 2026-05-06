# Security-First Coding Guidelines (.NET + React)

## Purpose

The primary goal is to produce secure, maintainable code by default for .NET backends and React frontends.

## Scope

- Applies to all coding tasks in this workspace.
- Prioritize prevention of security defects over feature speed.
- Favor least privilege, secure defaults, and explicit validation.

## General Security Rules

1. Treat all external input as untrusted.
2. Validate input at boundaries and encode output by context.
3. Never hardcode secrets, keys, tokens, or connection strings in source files.
4. Use environment variables or secure secret stores.
5. Prefer parameterized queries and ORM protections to avoid injection.
6. Log security-relevant events without logging sensitive data.
7. Fail safely with generic error messages to clients.
8. Keep dependencies patched and avoid known-vulnerable packages.
9. Use HTTPS/TLS and secure headers by default.
10. Follow Microsoft Docs MCP guidance when uncertain about security patterns.

## .NET Security Standards

1. Authentication and authorization:

- Use ASP.NET Core authentication middleware and policy-based authorization.
- Deny by default and grant access explicitly.

2. Input validation and model binding:

- Use DataAnnotations and server-side validation for all API inputs.
- Reject unexpected fields and enforce strict DTOs.

3. Data access:

- Use Entity Framework with parameterized operations.
- Avoid dynamic SQL unless absolutely necessary and safely parameterized.

4. API hardening:

- Enable rate limiting where appropriate.
- Add anti-forgery protections for cookie-based flows.
- Configure CORS to explicit origins, methods, and headers only.

5. Secrets and configuration:

- Use User Secrets (dev), Key Vault (cloud), and environment variables.
- Keep `.env` and config templates free from real credentials.

6. Transport and headers:

- Enforce HTTPS redirection and HSTS in production.
- Add secure headers (CSP, X-Content-Type-Options, frame protections) where applicable.

## React Security Standards

1. XSS prevention:

- Avoid `dangerouslySetInnerHTML` unless data is sanitized with a vetted library.
- Encode and sanitize any rich text from external sources.

2. Auth token handling:

- Prefer secure, HttpOnly cookies when architecture allows.
- If tokens are in browser storage, minimize lifetime and exposure.

3. API usage:

- Do not trust client-side checks as security controls.
- Validate authorization on the server for every protected action.

4. Routing and state:

- Protect sensitive routes with server-backed auth checks.
- Avoid exposing secrets in bundled frontend code.

5. Dependency hygiene:

- Keep npm dependencies current.
- Remove unused packages to reduce attack surface.

## Secure Coding Workflow

1. Before coding:

- Identify trust boundaries, sensitive data, and abuse paths.

2. During coding:

- Add validation, authorization, and safe error handling as first-class requirements.

3. Before completion:

- Verify no secrets were introduced.
- Check for common OWASP risks relevant to the change.
- Confirm secure defaults remain intact.

## Documentation and References

- Use concise Markdown and keep security notes close to implementation decisions.
- Prefer links to official Microsoft security docs and OWASP resources.
- Use Microsoft Docs MCP for up-to-date .NET and Azure security references.
