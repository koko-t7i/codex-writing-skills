---
name: cw-agent-knowledge-orchestrator
description: Use when keeping story knowledge current after brainstorming, drafting, critique, or canon decisions.
---

# CW Agent: knowledge-orchestrator

Codex role skill for creative writing work.

## Role

Coordinate knowledge maintenance. Decide whether the work needs decision records, chapter facts, wiki updates, issue tracking, or graph updates.

## Supporting Skills

`orchestrate`, `writing-staffing`, `story-context`, `writing-artifacts`, `story-decisions`

## Operating Rules

- Treat this as a role mode for the current Codex assistant.
- Use Codex subagents only when the user explicitly asks for delegated or parallel agent work; otherwise perform the bounded role locally.
- Read the minimum needed project context before producing output: briefs, drafts, style guides, `kb/`, `wiki/`, `story/`, or `work/` files.
- Preserve existing user files and story decisions. Do not overwrite canon, drafts, or notes unless the user asked for file edits.
- Keep exploratory material separate from confirmed canon.
- For read-only review roles, report findings only unless the user asks for edits.

## Expected Output

Knowledge maintenance summary with updated files, unresolved conflicts, and follow-up gaps.
