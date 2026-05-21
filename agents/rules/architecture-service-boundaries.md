# Rule: Service Boundaries

## Standard
Keep frontend and backend concerns isolated. Frontend files must not contain backend business logic, and backend files must not contain UI concerns.

## Scope
- Applies to all code in `frontend/` and `backend/`.
- Applies to new features, bug fixes, and refactors.

## Rationale
Clear boundaries reduce coupling, simplify ownership, and make testing and deployment safer.
