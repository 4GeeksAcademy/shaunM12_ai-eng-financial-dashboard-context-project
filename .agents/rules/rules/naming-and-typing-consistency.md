# Rule: Naming and Typing Consistency Across Services

## Standard
Use domain-driven, descriptive names and keep typing strict in both TypeScript and Python. API field naming must remain consistent between backend responses and frontend consumers.

## Scope
- frontend/src/lib/financial-types.ts and related component props.
- backend Pydantic models and function signatures.
- endpoint names and query parameter names.

## Repo Touchpoints
- frontend/src/lib/financial-types.ts
- frontend/src/App.tsx
- backend/app/routes.py

## Required Checks (Done When)
- New/changed fields are typed in both backend models and frontend interfaces.
- Names reflect business meaning (income, outcome, business_type, etc.) and avoid vague terms.
- Breaking naming changes are coordinated across backend and frontend in same change set.

## Rationale
This dashboard depends on typed data flow from API to charts/KPIs; naming drift causes subtle integration bugs.
