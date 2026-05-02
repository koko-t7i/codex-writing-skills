---
name: cw-command-bs
description: Use when the user types /bs, asks for brainstorm mode, or wants to explore story ideas before committing to canon.
---

# CW Command: /bs

Codex command-entry skill for the creative writing workflow.

## Route

Use `brainstorming` or `cw-agent-brainstormer` depending on whether the user needs direct work or a role-specific workflow.

## Behavior

- Explore possibilities without treating suggestions as canon.
- Capture user-stated facts plainly.
- Mark assistant suggestions with `<AI>...</AI>`.
- Mark author-only secrets or spoiler material with `<hidden>...</hidden>`.
- Preserve uncertainty with `[TBD]`.
- End with useful next questions or option clusters.

## Input Handling

Treat text after `/bs` as the command argument. If the user provides only the command and the missing target would block useful work, ask one focused question for the missing topic, draft, file, or goal.
