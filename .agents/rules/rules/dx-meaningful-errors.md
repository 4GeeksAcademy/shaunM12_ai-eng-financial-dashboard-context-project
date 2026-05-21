# Rule: Meaningful and Actionable Error Messages

## Standard
Expose clear, actionable error messages to users and developers while keeping sensitive internals private.

## Scope
- Frontend UI error states and fetch/network failures.
- Backend validation and runtime error responses.

## Repo Touchpoints
- frontend/src/App.tsx
- backend/app/routes.py
- backend/app/main.py

## Required Checks (Done When)
- User-facing messages explain what happened and next action (retry/check API/config).
- Developer diagnostics are available in logs, not in client payloads.
- Unknown failures fall back to a generic safe message.

## Rationale
The dashboard depends on remote API calls. Good error UX lowers support/debug time without increasing security risk.
