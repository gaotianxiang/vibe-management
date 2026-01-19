# Decisions (Append-only)

## ADR-0001: Markdown as canonical project memory
Date: 2026-01-19
Context:
LLMs forget context across sessions and have limited context windows.
Decision:
All project state (context, progress, decisions, logs) will live in markdown files.
Alternatives considered:
- Rely on LLM memory (rejected)
- Store state only in code comments (rejected)
Consequences:
- Requires disciplined updates
- Enables full resumability and auditability

## ADR-0002: LLMs may only propose edits
Date: 2026-01-19
Context:
Direct LLM writes risk corruption of canonical state.
Decision:
LLMs must output unified diffs; humans apply changes.
Consequences:
- More friction
- Strong safety and traceability
