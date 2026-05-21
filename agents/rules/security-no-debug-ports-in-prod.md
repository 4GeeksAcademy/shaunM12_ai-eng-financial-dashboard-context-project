# Rule: No Debug Ports in Production

## Standard
Do not expose debugger ports or run debugger processes in production containers.

## Scope
- Applies to Dockerfiles, compose files, and runtime commands.
- Applies to backend services and any future worker services.

## Rationale
Debugger exposure can allow code introspection or execution paths not intended for production.
