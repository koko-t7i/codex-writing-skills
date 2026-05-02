---
name: cw-command-critique
description: Use when the user types /critique or wants structured feedback on fiction prose, plot, pacing, character, dialogue, or genre fit.
---

# CW Command: /critique

Codex command-entry skill for the creative writing workflow.

## Route

Use `prose-critique` or `cw-agent-critic` depending on whether the user needs direct work or a role-specific workflow.

## Behavior

- Critique existing story content; do not rewrite unless asked.
- Calibrate feedback to draft stage and requested focus.
- Use concrete textual evidence and severity.
- Cover reader impact, not just abstract craft rules.
- Ask for the text or focus only if it is missing.

## Input Handling

Treat text after `/critique` as the command argument. If the user provides only the command and the missing target would block useful work, ask one focused question for the missing topic, draft, file, or goal.
