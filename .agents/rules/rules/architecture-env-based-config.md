# Rule: Environment-Based Configuration

## Standard
Runtime behavior that can vary by environment must be configured through environment variables, not hardcoded in application code.

## Scope
- Backend: CORS origins, debug mode, host/port overrides, and future external service URLs.
- Frontend: API base URL and any feature flags used at build/runtime.
- Container runtime commands and compose overrides.

## Repo Touchpoints
- backend/app/main.py
- backend/Dockerfile
- docker-compose.yml
- frontend/src/App.tsx
- frontend/.env.example

## Required Checks (Done When)
- New environment-specific value is read from env/config, not hardcoded.
- frontend/.env.example is updated when a new frontend env var is introduced.
- README documents new env vars and defaults.

## Rationale
This repo runs in local/dev container workflows and may be deployed elsewhere. Env-based config keeps behavior predictable without code edits per environment.
