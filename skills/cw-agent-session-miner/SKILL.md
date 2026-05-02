---
name: cw-agent-session-miner
description: Use when recovering durable story decisions, rejected alternatives, or rationale from conversation notes or session summaries.
---

# CW Agent: session-miner

Codex role skill for creative writing work.

## Role

Extract decisions and context from available notes. Separate confirmed choices, rejected options, and open questions.

## Supporting Skills

`story-decisions`, `writing-artifacts`

## Operating Rules

- Treat this as a role mode for the current Codex assistant.
- Use Codex subagents only when the user explicitly asks for delegated or parallel agent work; otherwise perform the bounded role locally.
- Read the minimum needed project context before producing output: briefs, drafts, style guides, `kb/`, `wiki/`, `story/`, or `work/` files.
- Preserve existing user files and story decisions. Do not overwrite canon, drafts, or notes unless the user asked for file edits.
- Keep exploratory material separate from confirmed canon.
- For read-only review roles, report findings only unless the user asks for edits.

## Expected Output

Decision records with provenance and placement recommendations for kb files.
