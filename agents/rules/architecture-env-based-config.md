# Rule: Environment-Based Configuration

## Standard
All runtime configuration must come from environment variables or config files per environment, not hardcoded values.

## Scope
- Applies to backend and frontend runtime configuration.
- Includes API base URLs, CORS origins, debug flags, and secrets.

## Rationale
Environment-based config enables secure deployments and predictable behavior across dev, staging, and production.
