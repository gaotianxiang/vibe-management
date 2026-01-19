# Scope & Boundaries (Monorepo-Safe)

## Owned folders (LLM may modify)
- //path/to/project/...
- //path/to/another/...

## Read-only dependencies (LLM may read, must not edit)
- //path/to/deps/...

## Forbidden areas (do not touch)
- //...

## Entry points
Build:
- <command>

Test:
- <command>

Lint:
- <command>

## Constraints
- Language-agnostic; do not assume framework unless in CONTEXT/SOURCES.
- Prefer minimal blast radius changes.
- Always update PROGRESS + CHANGELOG at checkpoint.

## Interfaces / Integration points
- Inputs:
- Outputs:
- APIs:
