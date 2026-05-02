---
name: cw-router
description: Use when choosing the right Codex creative writing skill, workflow skill, or role skill for brainstorming, drafting, critique, documentation, story structure, or knowledge maintenance.
---

# Creative Writing Router

Use this router to pick the smallest useful Codex skill for a writing task.

## Workflow Skills

| User intent | Skill |
|---|---|
| Explore ideas | `cw-brainstorm` |
| Draft or revise prose | `cw-write` |
| Document finalized canon | `cw-wiki` |
| Critique existing prose | `cw-critique` |

## Role Skills

| Need | Skill |
|---|---|
| End-to-end story workflow | `cw-agent-story-orchestrator` |
| Draft/revision loop | `cw-agent-draft-orchestrator` |
| Prose drafting | `cw-agent-writer` |
| Adversarial critique | `cw-agent-critic` |
| Reader experience report | `cw-agent-reader-sim` |
| Brainstorming | `cw-agent-brainstormer` |
| Outlining | `cw-agent-outliner` |
| Wiki/documentation | `cw-agent-wiki-editor` |
| Continuity checking | `cw-agent-continuity-checker` |
| Style guide creation | `cw-agent-style-creator` |
| Context gathering | `cw-agent-explorer` |
| External research | `cw-agent-researcher` |
| Knowledge maintenance | `cw-agent-knowledge-orchestrator` |

## Core Knowledge Skills

Use these directly when the user asks for the method rather than a role:

- `brainstorming`: exploratory idea capture
- `prose-writing`: drafting narrative fiction
- `prose-critique`: structured feedback
- `story-architecture`: arcs, chapters, scenes, pacing
- `story-context`: choosing and loading relevant context
- `story-decisions`: recording choices and rejected alternatives
- `wiki-docs`: finalized reference documentation
- `writing-artifacts`: file conventions for `story/`, `wiki/`, `kb/`, and `work/`
- `writing-issues`: tracking recurring writing problems
- `writing-principles`: reader reward channels and AI writing failure modes
- `writing-staffing`: choosing which Codex role skill should handle a task
- `orchestrate`: coordinating multi-step writing workflows

## Decision Rules

- Still exploring: use `brainstorming` or `cw-agent-brainstormer`.
- Ready to draft: use `prose-writing` or `cw-agent-writer`.
- Ready to document: use `wiki-docs` or `cw-agent-wiki-editor`.
- Needs feedback: use `prose-critique` or `cw-agent-critic`.
- Needs the full workflow: use `cw-agent-story-orchestrator`.
- Use Codex subagents only when the user explicitly asks for delegated or parallel agent work.
