# Rule: API Contract Changes Must Be Documented

## Standard
When endpoint path, query params, response fields, or status behavior change, documentation must be updated in the same change set.

## Scope
- backend route definitions and Pydantic response models.
- README/API usage notes and examples consumed by frontend.

## Repo Touchpoints
- backend/app/routes.py
- README.md
- frontend/src/App.tsx

## Required Checks (Done When)
- Route/model change is reflected in code-level contract (typing/response model).
- README/API usage notes are updated when integration expectations change.
- Frontend callers are updated if backend contract changed.

## Rationale
This project depends on frontend/backend contract alignment; stale docs quickly create integration regressions.
