# Rule: Restrictive CORS Outside Local Development

## Standard
Wildcard CORS ("*") is allowed only for local development. Non-local environments must use an explicit allowlist from environment config.

## Scope
- backend/app/main.py CORS middleware settings.
- Any deployment configuration that defines allowed origins.

## Repo Touchpoints
- backend/app/main.py
- docker-compose.yml
- backend/Dockerfile

## Required Checks (Done When)
- Non-local config does not use allow_origins=["*"].
- Allowed origins come from configuration, not literals in code.
- README documents local vs non-local CORS behavior.

## Rationale
Current wildcard CORS is convenient for dev but unsafe as a deployment default.
