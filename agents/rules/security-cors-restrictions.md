# Rule: Restrictive CORS in Non-Local Environments

## Standard
Use explicit allowed origins in non-local environments. Wildcard CORS is allowed only for local development.

## Scope
- Applies to backend CORS middleware configuration.
- Applies to all deployable environments.

## Rationale
Restrictive CORS lowers cross-origin abuse risk and limits unintended API exposure.
