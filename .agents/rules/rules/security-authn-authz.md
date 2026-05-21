# Rule: Authentication and Authorization Defaults

## Standard
New backend endpoints are private by default unless explicitly declared public. Public endpoints must be intentionally limited and documented.

## Scope
- backend/app/routes.py and future route modules.
- Applies to all /api paths, except explicitly public endpoints (for example /health).

## Repo Touchpoints
- backend/app/routes.py
- backend/tests/test_routes.py

## Required Checks (Done When)
- Endpoint access level (public/private) is documented in code or docs.
- Private endpoints include auth dependency and role checks as required.
- Tests include at least one unauthorized/forbidden path for protected endpoints.

## Rationale
The current repo is open for learning. This rule ensures future production-oriented additions do not accidentally stay unauthenticated.
