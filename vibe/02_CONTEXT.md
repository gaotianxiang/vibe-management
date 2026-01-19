# Curated Context (must-load)

## Invariants
- LLMs are stateless across sessions.
- Context windows are limited and lossy.
- Humans currently act as progress trackers.
- Markdown files are the canonical project memory.
- LLMs must propose diffs; humans approve.

## Key terminology
- Vibe coding: exploratory, LLM-driven development across sessions.
- Canonical state: markdown files treated as ground truth.
- Context ingestion: process of distilling new info into SOURCES + CONTEXT.

## Repo conventions
- commands/vibe/: Gemini CLI custom commands
- templates/: canonical markdown templates for projects
- Unified diffs are the only allowed mutation format.

## High-level system summary
- Project state is externalized into structured markdown.
- Gemini CLI commands orchestrate session lifecycle.
- Sessions are explicit, checkpointed, and resumable.

## Active constraints / gotchas
- CONTEXT.md must stay small and curated.
- Large materials go into SOURCES (or equivalent).
