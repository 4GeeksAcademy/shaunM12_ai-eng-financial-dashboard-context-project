# Rule: Debugger Tooling Is Dev-Only

## Standard
Debugger runtime (debugpy) and debug ports (for example 5678) must be enabled only in dev profiles, never in production images/manifests.

## Scope
- backend/Dockerfile
- docker-compose.yml
- CI/deployment container definitions

## Repo Touchpoints
- backend/Dockerfile
- docker-compose.yml

## Required Checks (Done When)
- Production build/run command does not include debugpy.
- Production manifests do not expose debugger ports.
- Dev/debug settings are isolated in dev-specific profile/target.

## Rationale
The current backend image starts with debugpy and exposes 5678. This is useful for local debugging but risky for production deployment.
