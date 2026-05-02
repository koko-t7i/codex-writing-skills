---
name: cw-brainstorm
description: Use when the user wants a Codex creative writing brainstorming workflow for story ideas, plot, characters, worldbuilding, chapters, scenes, or unresolved creative choices.
---

# CW Brainstorm

Codex workflow skill for exploratory creative writing work.

## Route

Use `brainstorming` or `cw-agent-brainstormer` depending on whether the user needs quick idea capture or a role-specific brainstorm report.

## Behavior

- Explore possibilities without treating suggestions as canon.
- Capture user-stated facts plainly.
- Mark assistant suggestions with `<AI>...</AI>`.
- Mark author-only secrets or spoiler material with `<hidden>...</hidden>`.
- Preserve uncertainty with `[TBD]`.
- End with useful next questions or option clusters.

## Input Handling

Treat the user's prompt as the brainstorm topic. If the topic is missing, ask one focused question for the story problem, scene, character, or worldbuilding area to explore.
