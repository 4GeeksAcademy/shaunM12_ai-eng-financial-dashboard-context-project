# Rule: Persistent Data for Production Paths

## Standard
Do not use generated in-memory datasets for production-facing workflows. Use a persistent data layer for any feature intended beyond demo mode.

## Scope
- Applies to backend data retrieval and storage logic.
- Excludes explicit demo-only endpoints clearly marked as mock.

## Rationale
Persistent storage improves reliability, reproducibility, and auditability.
