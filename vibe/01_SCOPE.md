# Scope & Boundaries (Meta-project)

## Owned folders
- ./commands/vibe/...
- ./templates/...

## Read-only dependencies
- Gemini CLI behavior and command resolution
- LLM behavior (Gemini / Codex / Claude)

## Forbidden areas
- Modifying Gemini CLI internals
- Assuming persistent LLM memory across sessions

## Entry points
Build:
- N/A (documentation + workflow system)

Test:
- Manual validation via Gemini CLI

Lint:
- Markdown linting (optional)

## Constraints
- Language-agnostic by design.
- Must work with monorepos and partial folder scopes.
- Markdown is the single source of truth.
- LLMs may only propose edits, never overwrite canon.

## Interfaces / Integration points
- Gemini CLI custom commands
- Future Codex / Claude command parity
