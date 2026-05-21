# Rule: Frontend/Backend Service Boundaries

## Standard
Keep UI/rendering logic in frontend and API/data generation logic in backend. Cross-service coupling must happen only through HTTP contracts.

## Scope
- frontend/: React components, chart formatting, view-state handling.
- backend/: route handlers, filtering/aggregation, response models.

## Repo Touchpoints
- frontend/src/App.tsx
- frontend/src/components/dashboard/
- frontend/src/lib/financial-utils.ts
- backend/app/main.py
- backend/app/routes.py

## Required Checks (Done When)
- Frontend does not import Python/backend code.
- Backend does not include UI formatting/presentation concerns.
- Contract changes (field names, endpoint params) update both backend and frontend callers.

## Rationale
This repo already follows separate service folders. Enforcing this keeps changes isolated and easier to test/deploy.
