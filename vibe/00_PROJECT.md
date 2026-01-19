# Project
Name: Vibe Coding Project Management System
Owner: Tianxiang Gao
Status: Active

## One-liner
Design a durable, LLM-friendly project management system that enables large, multi-session “vibe coding” on massive monorepos using Gemini CLI (initially), with markdown as the canonical memory.

## Goals
- Enable LLM-assisted development across many sessions without losing context.
- Externalize all project state into structured markdown.
- Support monorepo-scale codebases (millions of LOC).
- Allow semi-automated workflows where LLM proposes edits and human approves.
- Produce verbose, structured logs suitable for future meta-optimization.

## Non-goals
- Full automation without human approval.
- Storing entire source trees as LLM context.
- Tool-specific lock-in beyond Gemini CLI v1.

## Success criteria (Definition of Done)
- A standard `vibe/` project structure exists and is reusable.
- Gemini CLI custom commands (`/vibe:*`) can drive sessions end-to-end.
- A project can be paused and resumed days later with no loss of intent.
- Logs are rich enough for LLM-driven workflow optimization.

## Stakeholders
- Primary: Human developer (solo) + LLM
