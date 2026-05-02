---
name: cw-wiki
description: Use when the user wants a Codex creative writing documentation workflow for finalized story canon, wiki pages, lore entries, character pages, or reference docs.
---

# CW Wiki

Codex workflow skill for finalized story documentation.

## Route

Use `wiki-docs` or `cw-agent-wiki-editor` depending on whether the user needs a direct page draft or a role-specific documentation workflow.

## Behavior

- Document only finalized information.
- Use citations or source anchors when available.
- Write in polished, neutral, third-person reference style.
- Add cross-links where useful.
- If the user is still exploring, route to `cw-brainstorm` or `brainstorming`.

## Input Handling

Treat the user's prompt as the documentation target. If the target or canon status is missing, ask one focused question.
