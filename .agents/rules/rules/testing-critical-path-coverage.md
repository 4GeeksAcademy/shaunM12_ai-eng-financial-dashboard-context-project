# Rule: Critical Path Test Coverage for Changes

## Standard
Changes to business logic or API contracts must include tests for primary behavior and at least one edge/failure path.

## Scope
- Backend endpoint behavior and filter/aggregation logic.
- Frontend calculation/formatting utilities and key data-driven UI states.

## Repo Touchpoints
- backend/tests/test_routes.py
- frontend/src/lib/financial-utils.test.ts
- frontend/src/components/dashboard/

## Required Checks (Done When)
- Backend endpoint change: add or update request/response test in backend/tests.
- Frontend data utility change: add or update Vitest case.
- Bug fix: include a regression test that fails before and passes after.

## Rationale
This repo already has a strong testing base. This rule keeps that strength aligned with future feature work.
