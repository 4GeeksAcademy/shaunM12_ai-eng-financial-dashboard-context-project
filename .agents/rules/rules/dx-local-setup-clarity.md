# Rule: Local Setup and Runbook Accuracy

## Standard
Repository setup/run/test instructions must be updated whenever commands, ports, dependencies, or env requirements change.

## Scope
- README files and onboarding notes.
- Backend and frontend local workflows (container and non-container where supported).

## Repo Touchpoints
- README.md
- backend/requirements.txt
- frontend/package.json
- docker-compose.yml

## Required Checks (Done When)
- README includes current run command(s), service URLs, and API docs URL.
- README includes test command(s) for backend/frontend.
- New env vars or port changes are documented in the same update.

## Rationale
Most contributor friction in this repo comes from setup mismatch, not code complexity.
