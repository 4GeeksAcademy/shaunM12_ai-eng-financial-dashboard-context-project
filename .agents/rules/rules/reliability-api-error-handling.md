# Rule: Consistent and Safe API Error Handling

## Standard
Backend endpoints must return predictable, sanitized error responses and use centralized exception handling for common failure modes.

## Scope
- backend/app/main.py middleware/handlers
- backend/app/routes.py endpoints
- validation and runtime exception paths

## Repo Touchpoints
- backend/app/main.py
- backend/app/routes.py
- backend/tests/test_routes.py

## Required Checks (Done When)
- Known failures map to intentional status codes.
- Error payloads are structured and safe for clients (no stack traces/internal details).
- Tests cover at least one negative/error path for changed endpoint behavior.

## Rationale
Current success-path coverage is good. Standardized error behavior is needed so frontend handling remains stable as APIs evolve.
