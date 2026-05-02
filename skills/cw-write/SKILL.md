---
name: cw-write
description: Use when the user wants a Codex creative writing prose workflow for drafting or revising fiction, optionally with a style, genre, scene brief, chapter target, or critique synthesis.
---

# CW Write

Codex workflow skill for drafting and revising narrative prose.

## Route

Use `prose-writing` or `cw-agent-writer` depending on whether the user needs direct prose or a role-specific drafting workflow.

## Behavior

- Write narrative prose, not outline notes or critique.
- Look for available style guides, character profiles, lore docs, and prior chapters before drafting.
- If a style name is provided and no project guide exists, use general conventions for that style and say so briefly.
- If the request is actually style-guide creation, route to `cw-agent-style-creator`.

## Input Handling

Treat the user's prompt as the writing brief. If the target is missing, ask one focused question for the scene, chapter, revision target, or style requirement.
