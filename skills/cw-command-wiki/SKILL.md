---
name: cw-command-wiki
description: Use when the user types /wiki or wants finalized story canon documented as wiki, lore, character, or reference pages.
---

# CW Command: /wiki

Codex command-entry skill for the creative writing workflow.

## Route

Use `wiki-docs` or `cw-agent-wiki-editor` depending on whether the user needs direct work or a role-specific workflow.

## Behavior

- Document only finalized information.
- Use citations or source anchors when available.
- Write in polished, neutral, third-person reference style.
- Add cross-links where useful.
- If the user is still exploring, route to `cw-command-bs` or `brainstorming`.

## Input Handling

Treat text after `/wiki` as the command argument. If the user provides only the command and the missing target would block useful work, ask one focused question for the missing topic, draft, file, or goal.
