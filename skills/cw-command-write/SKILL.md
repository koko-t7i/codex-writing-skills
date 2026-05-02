---
name: cw-command-write
description: Use when the user types /write, asks for prose-writing mode, or provides an optional style name plus a scene or revision request.
---

# CW Command: /write

Codex command-entry skill for the creative writing workflow.

## Route

Use `prose-writing` or `cw-agent-writer` depending on whether the user needs direct work or a role-specific workflow.

## Behavior

- Write narrative prose, not outline notes or critique.
- Look for available style guides, character profiles, lore docs, and prior chapters before drafting.
- If a style name is provided and no project guide exists, use general conventions for that style and say so briefly.
- If the request is actually style-guide creation, route to `cw-agent-style-creator`.

## Input Handling

Treat text after `/write` as the command argument. If the user provides only the command and the missing target would block useful work, ask one focused question for the missing topic, draft, file, or goal.
