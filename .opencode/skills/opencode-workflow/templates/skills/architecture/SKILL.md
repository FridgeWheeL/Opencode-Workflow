---
name: architecture
description: Use when designing or reviewing the project structure. Covers architecture layers, dependency rules, and conventions.
---

# Architecture Standards

See `docs/Architecture/architecture.md` for the full architecture
documentation. This skill covers rules and conventions.

## Agent-managed content

This skill is maintained dynamically by the `@architect` agent. As the
project evolves and new patterns are discovered, the architect should
update this file to reflect what's actually in use.

When the architect detects any of the following, it should update the
relevant section below:

- A project structure pattern (monolith, modular monolith, microservices)
- An architecture pattern (layered, hexagonal, clean, onion, N-tier)
- Specific frameworks (CQRS, event sourcing, MediatR, etc.)
- Dependency injection approach
- Error/exception handling conventions
- Testing strategy that affects architecture
- Any other project-wide convention

Do not remove content that another agent or the user has added — only
add to or refine it.

## Project structure

{{PROJECT_STRUCTURE}}

## Architecture pattern

{{ARCH_PATTERN_DESCRIPTION}}

## Dependency rules

{{DEPENDENCY_RULES}}

## Conventions

{{ARCHITECTURE_CONVENTIONS}}

## Project roles

{{PROJECT_ROLES_TABLE}}
