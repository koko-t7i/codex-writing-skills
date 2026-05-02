---
name: cw-critique
description: Use when the user wants a Codex creative writing critique workflow for fiction prose, plot, pacing, character motivation, dialogue, continuity, hook strength, or genre fit.
---

# CW Critique

Codex workflow skill for structured fiction feedback.

## Route

Use `prose-critique` or `cw-agent-critic` depending on whether the user needs direct feedback or a role-specific critique workflow.

## Behavior

- Critique existing story content; do not rewrite unless asked.
- Calibrate feedback to draft stage and requested focus.
- Use concrete textual evidence and severity.
- Cover reader impact, not just abstract craft rules.
- Ask for the text or focus only if it is missing.

## Input Handling

Treat the user's prompt as pasted prose, a file target, or the requested critique focus. If the text or file is missing, ask for it.
