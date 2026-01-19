# Architecture

## Current system
- Stateless LLMs operate over:
  - Canonical markdown state
  - Explicit session objectives
- Gemini CLI provides:
  - Command namespace
  - File injection into prompts
- Human acts as:
  - Approver
  - Executor (build/test/lint)
  - Final arbiter

## Data flow
1. Human loads canonical markdown via Gemini CLI command.
2. LLM analyzes state and proposes diffs.
3. Human reviews and applies diffs.
4. Progress and logs are updated.
5. Session ends with a checkpoint.

## Design rules
- Markdown > LLM memory.
- Append-only logs.
- Small curated context, large external sources.
- Explicit session boundaries.
