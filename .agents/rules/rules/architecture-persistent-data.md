# Rule: Persistent Data for Non-Demo Features

## Standard
Mock/in-memory data is allowed only for explicit demo/training flows. Any feature intended for real usage must read/write persistent storage.

## Scope
- Backend endpoints under /api/metrics and future business endpoints.
- Data access and aggregation logic in backend/app/routes.py or extracted service/repository modules.

## Repo Touchpoints
- backend/app/routes.py
- backend/tests/test_routes.py

## Required Checks (Done When)
- If endpoint is demo-only, it is labeled in route docs/comments as mock/demo.
- If endpoint is non-demo, it uses a storage abstraction (repository/service) backed by persistent storage.
- Tests cover persistence-backed behavior (not only generated fixtures).

## Rationale
Current generated data is useful for bootstrapping. This rule prevents demo assumptions from leaking into production-oriented work.
