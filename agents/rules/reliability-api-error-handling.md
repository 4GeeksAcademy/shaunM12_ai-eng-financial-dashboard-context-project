# Rule: Consistent API Error Handling

## Standard
Use structured, user-safe error responses and centralized exception handling. Do not expose stack traces to clients.

## Scope
- Applies to all backend route handlers and middleware.
- Applies to validation and unexpected runtime exceptions.

## Rationale
Consistent handling improves client resilience and prevents accidental information leakage.
